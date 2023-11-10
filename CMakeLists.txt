cmake_minimum_required(VERSION 3.26)
project(calculadora_RPN C)

set(CMAKE_C_STANDARD 11)

#add_subdirectory(../Bibliotecas/libprg)
include(FetchContent)

FetchContent_Declare(
        libprg
        GIT_REPOSITORY https://github.com/JamillyS/Bibliotecas.git
        GIT_TAG origin/main
        #or GIT_TAG 0.0.1

)
FetchContent_MakeAvailable(libprg)

add_executable(calculadora_RPN main.c)

target_link_libraries(calculadora_RPN PUBLIC libprg)