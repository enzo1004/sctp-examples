CMAKE_MINIMUM_REQUIRED(VERSION 2.8)
PROJECT("echo server")

SET(CMAKE_C_FLAGS "-g -std=c99 -pthread -Wall -isystem")
SET(EXECUTABLE_OUTPUT_PATH ${PROJECT_BINARY_DIR}/bin)

ADD_EXECUTABLE(echoSCTPServerRecvmsg echoServer.c)

IF(${CMAKE_SYSTEM_NAME} MATCHES "Darwin")
  TARGET_LINK_LIBRARIES(echoSCTPServerRecvmsg /usr/lib/libsctp.dylib)
ENDIF(${CMAKE_SYSTEM_NAME} MATCHES "Darwin")

