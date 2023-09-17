cmake_minimum_required(VERSION 3.15) # Проверка версии CMake.
									# Если версия установленой программы
									# старее указаной, произойдёт аварийный выход.

project(algorithms_and_data_structures)

# Информация об используемом компиляторе (по умолчанию GNU,
#                                         по умолчанию стандрат C++17). См. cmake --system-information
if(CMAKE_CXX_COMPILER_LOADED)
    message(STATUS "CXX Compiler")
    message(STATUS "Compiler path: ${CMAKE_CXX_COMPILER}")
    message(STATUS "Compiler ID: ${CMAKE_CXX_COMPILER_ID}")
    message(STATUS "Compiler version: ${CMAKE_CXX_COMPILER_VERSION}")
    message(STATUS "Compiler is part of GCC: ${CMAKE_COMPILER_IS_GNUCXX}")
endif()

if(CMAKE_CXX_COMPILER_LOADED)
    message(STATUS "C Compiler")
    message(STATUS "Compiler path: ${CMAKE_C_COMPILER}")
    message(STATUS "Compiler ID: ${CMAKE_C_COMPILER_ID}")
    message(STATUS "Compiler version: ${CMAKE_C_COMPILER_VERSION}")
    message(STATUS "Compiler is part of GCC: ${CMAKE_COMPILER_IS_GNUCC}")
endif()

# Интерфейсная библиотека, содержащая настройки вроде стандарта языка.
# add_library(common_properties INTERFACE)
# target_compile_features(common_properties INTERFACE cxx_std_14)

# Решение №1
add_executable(solution_1 src/question_1/main.cpp)
set_target_properties(solution_1 PROPERTIES
  CXX_STANDARD 14
  CXX_STANDARD_REQUIRED YES
  CXX_EXTENSIONS NO
  )

# Решение №2
# add_executable(solution_2 src/question_2/main.c)

# Решение №3
# add_executable(solution_3 src/question_3/main.c)
# add_executable(solution_3_test src/question_3/test.c)
