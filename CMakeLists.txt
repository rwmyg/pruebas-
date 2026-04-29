cmake_minimum_required(VERSION 3.13)

include(pico_sdk_import.cmake)

project(keypad_led_controller C CXX ASM)
set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 17)

pico_sdk_init()

add_executable(keypad_led_controller
  src/main.cpp
)

# For Arduino-style Keypad library usage, adapt includes/libraries in your environment.
# This CMake file documents canonical Pico SDK project structure.

target_include_directories(keypad_led_controller PRIVATE include)

target_link_libraries(keypad_led_controller pico_stdlib)

pico_add_extra_outputs(keypad_led_controller)
