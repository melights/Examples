cmake_minimum_required(VERSION 2.6)

Project(Parameters)

#######################################
set(Boost_USE_MULTITHREADED ON)
FIND_PACKAGE(Boost 1.38 COMPONENTS program_options required)

INCLUDE_DIRECTORIES(${INCLUDE_DIRECTORIES} ${Boost_INCLUDE_DIRS})
LINK_DIRECTORIES(${LINK_DIRECTORIES} ${Boost_LIBRARY_DIRS})

#######################################

ADD_EXECUTABLE(Parameters Parameters.cpp)
target_link_libraries(Parameters )

