cmake_minimum_required(VERSION 3.20)
project(Tomb4Plus LANGUAGES C CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_compile_definitions(BX_CONFIG_DEBUG=0)

add_subdirectory(TOMB4)

if (APPLE)
    target_link_options(tomb4plus PRIVATE -Wl,-ignore_auto_link)
endif()