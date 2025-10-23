cmake_minimum_required(VERSION 3.10)

project(CGALExample)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

if (WIN32)
    set(CMAKE_TOOLCHAIN_FILE "$ENV{VCPKG_ROOT}/scripts/buildsystems/vcpkg.cmake" CACHE STRING "")
endif()

find_package(CGAL REQUIRED)

add_executable(HelloWorld src/main.cpp)

target_link_libraries(HelloWorld CGAL::CGAL)