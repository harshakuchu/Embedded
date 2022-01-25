cmake_minimum_required(VERSION 3.0.0)

project(jenkinsexample_Project VERSION 1.0.0)

add_subdirectory(day01)
add_subdirectory(utils)

add_executable(jenkinsexample
        /var/lib/jenkins/workspace/pp2/day01/src/main.cpp)

target_link_libraries(jenkinsexample PRIVATE day01 utils)
