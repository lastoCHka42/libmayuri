cmake_minimum_required(VERSION 3.1)
project(mayuri C)

set(CMAKE_COLOR_MAKEFILE OFF)
set(MAYURI_VERSION_MAJOR 0)
set(MAYURI_VERSION_MINOR 1)
set(MAYURI_VERSION_PATCH 0)
set(MAYURI_VERSION_STRING "${MAYURI_VERSION_MAJOR}.${MAYURI_VERSION_MINOR}.${MAYURI_VERSION_PATCH}")

option(BUILD_SHARED_LIBS "Build libmayuri as a shared library" OFF)

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/include)

set(SRCS
  src/lm_dummy.c
  )

add_library(mayuri ${SRCS})
