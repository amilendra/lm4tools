cmake_minimum_required(VERSION 3.5 FATAL_ERROR)
project(lm4tools LANGUAGES C)
if (MSVC)
    # warning level 4 and all warnings as errors
    add_compile_options(/W4 /WX)
else()
    # lots of warnings and all warnings as errors
    add_compile_options(-Wall -Wextra -pedantic)
endif()

if (APPLE)
    add_compile_options(-D__APPLE__)
endif()

add_subdirectory(lm4flash)
