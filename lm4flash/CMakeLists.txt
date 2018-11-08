cmake_minimum_required(VERSION 3.5 FATAL_ERROR)

project(lm4flash LANGUAGES C)
find_library(usb-1.0 REQUIRED)

add_executable(lm4flash lm4flash.c)

target_compile_options(lm4flash
  PRIVATE
    -O2
)

target_link_libraries(lm4flash
  PRIVATE
    usb-1.0
)
