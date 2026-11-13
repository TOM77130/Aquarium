cmake_minimum_required(VERSION 3.5)

project(Proj_Aquar LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)


add_executable(Proj_Aquar
    main.cpp
    aquarium.h
    aquarium.cpp
    poisson.h
    poisson.cpp
    forme_poisson.cpp
)

include(GNUInstallDirs)
install(TARGETS Proj_Aquar
    LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
    RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
)

target_link_libraries(Proj_Aquar
    glfw
    GLEW
    libGLEW.so
    libGLU.so
    libGL.so)
