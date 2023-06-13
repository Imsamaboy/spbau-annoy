#cmake_minimum_required(VERSION 3.25)
#project(testing_annoy)
#
#set(CMAKE_CXX_STANDARD 23)
#set(CMAKE_CXX_STANDARD_REQUIRED ON)
#
#include_directories(E:/c++/testing-annoy/annoy/src)
##link_directories(E:/c++/testing-annoy/annoy/build)
#target_link_libraries(testing_annoy annoy)
#add_executable(testing_annoy main.cpp)
#
### Add the Annoy library
##add_subdirectory(E:/c++/testing-annoy/annoy)
##target_link_libraries(testing_annoy annoy)

cmake_minimum_required(VERSION 3.25)
project(testing_annoy)

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Установите путь к исходным файлам Annoy, если они находятся в E:/c++/testing-annoy/annoy/src
include_directories(E:/c++/testing-annoy/annoy/src)

#find_package(nlohmann_json 3.11.2 REQUIRED)

# Создайте исполняемый файл "testing_annoy" из main.cpp
add_executable(testing_annoy main.cpp)
#target_link_libraries(testing_annoy PRIVATE nlohmann_json::nlohmann_json)

# Связывание с библиотекой Annoy
target_link_libraries(testing_annoy PRIVATE E:/c++/testing-annoy/annoy/build/libannoy.a)
