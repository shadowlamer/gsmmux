cmake_minimum_required(VERSION 3.0)

set(TARGET gsmmuxd)

project(${TARGET})

#set(CMAKE_CXX_STANDARD 11) 
#set(CMAKE_CXX_STANDARD_REQUIRED on)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -Wextra -Werror")

AUX_SOURCE_DIRECTORY(. C_SOURCES)
add_executable( ${TARGET} ${C_SOURCES})

include_directories(.)

install(TARGETS ${TARGET} DESTINATION sbin)
