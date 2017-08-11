cmake_minimum_required(VERSION 3.2.1)
project(Tutorial)

option(USE_MYMATH "Use tutorial provided math implementation" ON)

include_directories(${PROJECT_SOURCE_DIR})

if(USE_MYMATH)
    include_directories(${PROJECT_SOURCE_DIR}/Math)
    add_subdirectory(Math)
    set(EXTRA_LIBS ${EXTRA_LIBS} Math)
endif()

#adding .exe file
add_executable(Tutorial main.cpp)
target_link_libraries(Tutorial ${EXTRA_LIBS})