cmake_minimum_required(VERSION 3.5)
project(dimgin)

find_package(GTest REQUIRED)

enable_testing()

add_executable(
  hello_test
  tests/array_tests.cpp
)
target_link_libraries(
  hello_test
  GTest::gtest_main
)

include(GoogleTest)
gtest_discover_tests(hello_test)
