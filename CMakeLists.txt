cmake_minimum_required(VERSION 3.16)

project(QtTest)

find_package(Qt5 COMPONENTS Core Widgets Network Svg Qml Quick QuickWidgets REQUIRED)

set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(SOURCES main.cpp)

add_executable(QtTest ${SOURCES})

set_property(TARGET QtTest PROPERTY CSS_STANDARD 17)
