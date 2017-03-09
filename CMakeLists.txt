cmake_minimum_required(VERSION 3.1 FATAL_ERROR)
project(mammoth)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

enable_testing()

add_executable(mammoth
    src/compiler.cpp
    src/lexer.cpp
)

add_executable(test_lexer
    src/test/test_lexer.cpp
    src/lexer.cpp
)

add_test(test_lexer ${CMAKE_CURRENT_BINARY_DIR}/test_lexer)