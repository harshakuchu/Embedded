add_executable(test
        /var/lib/jenkins/workspace/pp2/day01/unit_tests/day1-gtests
        /var/lib/jenkins/workspace/pp2/day01/src/day1.cpp
        /var/lib/jenkins/workspace/pp2/day01/include/day02/day1.h)
       
target_include_directories(test PRIVATE include)

enable_testing()
add_test(NAME test COMMAND test)
