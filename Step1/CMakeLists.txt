cmake_minimum_required(VERSION 3.5.2) #Adding minimum cmake version
project(Tutorial) #Name of the project

# add the binary tree to the search path for include files
# so that we will find variables.h
include_directories(variables.h)

add_executable(Tutorial tutorial.cpp) #add_executable(ExecutableName executable.cpp)
