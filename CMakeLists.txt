cmake_minimum_required(VERSION 3.30.0)
project(LAB2 VERSION 0.1.0 LANGUAGES CXX)


set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)


add_executable(LAB2 
    main.cpp 
    spliter.cpp 
    utilite.cpp
)


enable_testing()
find_package(GTest REQUIRED)

add_executable(LAB2_tests tests.cpp spliter.cpp utilite.cpp)
target_link_libraries(LAB2_tests GTest::gtest_main)

include(GoogleTest)
gtest_discover_tests(LAB2_tests)