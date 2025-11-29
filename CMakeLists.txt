# min version of cmake
cmake_minimum_required(VERSION 3.10)

# name of project
project(PacketProcessing VERSION 1.0)

file(GLOB SOURCE_FILES "src/*.cpp")

add_executable(PacketProcessing ${SOURCE_FILES})
target_include_directories(PacketProcessing PUBLIC include)

