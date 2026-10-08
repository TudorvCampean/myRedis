cmake_minimum_required(VERSION 3.10.0)
project(myRedis VERSION 0.1.0 LANGUAGES C CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

#server
add_executable(server tcp_server.cpp)
target_compile_options(server PRIVATE -Wall -Wextra)

#client
add_executable(client tcp_client.cpp)
target_compile_options(client PRIVATE -Wall -Wextra)
