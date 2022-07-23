cmake_minimum_required(VERSION 3.0.0)
project(containers-generator VERSION 0.1.0 LANGUAGES C)

include(CTest)
enable_testing()

include (${CMAKE_SOURCE_DIR}/cmake/CompilerWarnings.cmake)
include (${CMAKE_SOURCE_DIR}/cmake/option.cmake)

set_choice(CMAKE_BUILD_TYPE "Debug;Release;MinSizeRel;RelWithDebInfo" "Debug" "Choose type of build")

set (SRCS
    src/main.c
)

set (HEADERS
)

add_executable(containers-generator ${SRCS} ${HEADERS})

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
