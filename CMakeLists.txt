cmake_minimum_required(VERSION 3.16)

project(QtTest)

find_package(Qt5 COMPONENTS Core Widgets Network Svg Qml Quick QuickWidgets REQUIRED)
find_package(Qt5QuickCompiler)

set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(SOURCES main.cpp)

set(LIBS Qt5::Core Qt5::Widgets Qt5::Svg Qt5::Qml Qt5::Quick Qt5::QuickWidgets)

qt5_use_modules(QtTest Quick Core)

add_executable(QtTest ${SOURCES})
target_link_libraries(QtTest ${LIBS})

set_property(TARGET QtTest PROPERTY CSS_STANDARD 17)
