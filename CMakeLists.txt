project(sandbox)

cmake_minimum_required(VERSION 3.7.0 FATAL_ERROR)

find_package(Qt5 COMPONENTS Core Network REQUIRED)
find_package(CutelystQt5 REQUIRED)

# Auto generate moc files
set(CMAKE_AUTOMOC ON)

# As moc files are generated in the binary dir, tell CMake
# to always look for includes there:
set(CMAKE_INCLUDE_CURRENT_DIR ON)

# Enable C++11 features
add_definitions(-std=c++11)

include_directories(
    ${CMAKE_SOURCE_DIR}
    ${CMAKE_CURRENT_BINARY_DIR}
    ${CutelystQt5_INCLUDE_DIR}
)
