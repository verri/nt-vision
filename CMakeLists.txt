cmake_minimum_required(VERSION 3.0)

# Na dúvida, coloque o Include Guard

project(nt_vision VERSION 1.0)

add_subdirectory(../nt-io nt-io)

add_library(nt_vision src/vision.cpp)

target_compile_features(nt_vision PRIVATE cxx_std_14)

target_include_directories(nt_vision PUBLIC include/)
target_link_libraries(nt_vision PRIVATE nt_io)
