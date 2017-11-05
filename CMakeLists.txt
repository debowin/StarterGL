cmake_minimum_required(VERSION 3.8)
project(StarterGL)

set(CMAKE_CXX_STANDARD 11)

set(MODEL_LOAD_SOURCE_FILES
        glad/glad.c
        glad/glad.h
        glad/khrplatform.h
        ModelLoad.cpp
        )

set(TRIANGLE_COLORED_SOURCE_FILES
        glad/glad.c
        glad/glad.h
        glad/khrplatform.h
        TriangleColored.cpp
        )

set(CUBE_3D_SOURCE_FILES
        glad/glad.c
        glad/glad.h
        glad/khrplatform.h
        Cube3D.cpp
        )

set(CUBE_LIT_1VBO_SOURCE_FILES
        glad/glad.c
        glad/glad.h
        glad/khrplatform.h
        CubeLit1VBO.cpp
        )

set(BLANK_SCREEN_SDL_SOURCE_FILES
        glad/glad.c
        glad/glad.h
        glad/khrplatform.h
        BlankScreenSDL.cpp
        )

set(LINKER_FLAGS "-lSDL2 -lSDL2main -lGL -ldl")
link_libraries("${LINKER_FLAGS}")

add_executable(BlankScreenSDL ${BLANK_SCREEN_SDL_SOURCE_FILES})
add_executable(TriangleColored ${TRIANGLE_COLORED_SOURCE_FILES})
add_executable(Cube3D ${CUBE_3D_SOURCE_FILES})
add_executable(CubeLit1VBO ${CUBE_LIT_1VBO_SOURCE_FILES})
add_executable(ModelLoad ${MODEL_LOAD_SOURCE_FILES})