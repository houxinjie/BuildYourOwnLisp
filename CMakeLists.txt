cmake_minimum_required (VERSION 2.6)
project (lisp C)

if (CMAKE_C_COMPILER_ID MATCHES "GNU|Clang")
    set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -std=c99 -Wall -ledit -lm")
endif()

add_library(mpc mpc.c)
add_executable(lisp lisp.c)
target_link_libraries(lisp mpc)
