cmake_minimum_required(VERSION 3.8.2)

project(karrier
        VERSION 0.0.1
        LANGUAGES CXX)

add_executable(karrier
        main.cpp)
target_compile_features(karrier
        PUBLIC cxx_std_11)
set_target_properties(karrier PROPERTIES
        CXX_EXTENSIONS OFF)

find_package(SDL2 
        REQUIRED)
target_link_libraries(karrier
        PUBLIC SDL2::SDL2) 
target_link_libraries(karrier
        PUBLIC SDL2::SDL2main)

install(
        TARGETS karrier
        RUNTIME
        DESTINATION bin)
        
