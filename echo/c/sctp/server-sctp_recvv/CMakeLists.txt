CMAKE_MINIMUM_REQUIRED(VERSION 3.2)
PROJECT("echo server")

SET(CMAKE_C_FLAGS "-std=c99 -Wall")
SET(EXECUTABLE_OUTPUT_PATH ${PROJECT_BINARY_DIR}/bin)

ADD_EXECUTABLE(echoServer echoServer.c)

IF(${CMAKE_SYSTEM_NAME} MATCHES "Darwin")
  TARGET_LINK_LIBRARIES(echoServer /usr/lib/libsctp.dylib)
ENDIF(${CMAKE_SYSTEM_NAME} MATCHES "Darwin")
