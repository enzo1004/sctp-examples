CMAKE_MINIMUM_REQUIRED(VERSION 2.8)
PROJECT("echo server")

INCLUDE_DIRECTORIES(SYSTEM "/usr/include")
set(CMAKE_INCLUDE_SYSTEM_FLAG_C "-isystem ")

SET(CMAKE_C_FLAGS "-std=c99 -Wall")
SET(EXECUTABLE_OUTPUT_PATH ${PROJECT_BINARY_DIR}/bin)

ADD_EXECUTABLE(echoServer echoServer.c)



