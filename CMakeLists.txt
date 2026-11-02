cmake_minimum_required(VERSION 3.5)

project(TP_note LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(TP_note main.cpp)

include(GNUInstallDirs)
install(TARGETS TP_note
    LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
    RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
)
