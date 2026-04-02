cmake_minimum_required(VERSION 3.10)
project(Test)

# 1. Сначала задаем пути вывода (лучше делать это до создания целей)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/bin)

# 2. Создаем исполняемый файл (цель "Test")
add_executable(Test
    source/main.cpp
)

# 3. Теперь, когда цель "Test" существует, привязываем к ней папку с заголовками
target_include_directories(Test PUBLIC include)
