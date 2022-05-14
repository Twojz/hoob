cmake_minimum_required(VERSION 3.13)

include(pico_sdk_import.cmake)

project(hoob)

pico_sdk_init()

add_executable(hoob src/main.c)

pico_enable_stdio_usb(hoob 1)
pico_enable_stdio_uart(hoob 0)

pico_add_extra_outputs(hoob)

target_link_libraries(hoob pico_stdlib)