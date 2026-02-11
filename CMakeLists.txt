cmake_minimum_required(VERSION 3.20)

# Nombre del proyecto y lenguaje
project(semana03_lienzo LANGUAGES CXX)

# Estándar C++
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

find_package(SDL2 REQUIRED)

add_executable(lienzo
    main.cpp
)

# Vincular librerías SDL2
target_link_libraries(lienzo
    PRIVATE
    SDL2::SDL2main
    SDL2::SDL2
)

# Incluir directorios de SDL2
target_include_directories(lienzo PRIVATE ${SDL2_INCLUDE_DIRS})