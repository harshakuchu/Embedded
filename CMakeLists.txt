cmake_minimum_required(VERSION 3.0.0)

project(jenkinsexample_Project VERSION 1.0.0)

add_subdirectory(day01)
add_subdirectory(utils)

add_executable(jenkinsexample
        /home/harsha/workspace/pp1/day01/src/main.cpp
        /home/harsha/workspace/pp1/day01/src/day1.cpp
        /home/harsha/workspace/pp1/utils/src/FileLoader.cpp
        /home/harsha/workspace/pp1/utils/src/StringHelper.cpp)

target_link_libraries(jenkinsexample PRIVATE day01 utils)
