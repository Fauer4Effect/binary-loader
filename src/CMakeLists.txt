file(GLOB HEADER_LIST CONFIGURE_DEPENDS "${BinaryLoader_SOURCE_DIR}/include/*.hpp")

add_library(binary_loader_lib loader.cpp ${HEADER_LIST})

target_include_directories(binary_loader_lib PUBLIC ../include)

target_link_libraries(binary_loader_lib PRIVATE bfd)

target_compile_features(binary_loader_lib PUBLIC cxx_std_11)