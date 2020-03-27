cmake_minimum_required(VERSION 3.10)

project(QtTest)

set(SOURCES main.cpp)

add_executable(QtTest ${SOURCES})

set_property(TARGET ci_example PROPERTY CSS_STANDARD 17)
