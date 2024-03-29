cmake_minimum_required(VERSION 3.9)
project(engine_a VERSION 0.7.0 DESCRIPTION "Cross-Platform Multimedia Engine")
set(CMAKE_BUILD_TYPE Release)
set(CMAKE_CXX_STANDARD 17)
set(TZ_COMPILE_FLAGS "-Wall -Wextra -pedantic-errors -O3")
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} ${TZ_COMPILE_FLAGS}")
include_directories(engine_a ${PROJECT_SOURCE_DIR}/inc)
include_directories(engine_a ${PROJECT_SOURCE_DIR}/src)
link_directories(${PROJECT_SOURCE_DIR}/lib)
add_library(engine_a SHARED
        src/audio/audio.cpp
        src/audio/audio.hpp
        src/audio/audio.inl

        src/core/listener.cpp
        src/core/listener.hpp
        src/core/scene.cpp
        src/core/scene.hpp
        src/core/scene.inl
        src/core/topaz.hpp
        src/core/window.cpp
        src/core/window.hpp
        src/core/window.inl
        src/data/vector.hpp
        src/data/vector.inl

        src/data/matrix.cpp
        src/data/matrix.hpp
        src/data/quaternion.cpp
        src/data/quaternion.hpp
        src/data/transform.cpp
        src/data/transform.hpp

        src/graphics/asset.cpp
        src/graphics/asset.hpp
        src/graphics/asset.inl
        src/graphics/camera.cpp
        src/graphics/camera.hpp
        src/graphics/frame_buffer.cpp
        src/graphics/frame_buffer.hpp
        src/graphics/frame_buffer.inl
        src/graphics/glew.c
        src/graphics/graphics.cpp
        src/graphics/graphics.hpp
        src/graphics/graphics.inl
        src/graphics/light.cpp
        src/graphics/light.hpp
        src/graphics/mesh.cpp
        src/graphics/mesh.hpp
        src/graphics/shader.cpp
        src/graphics/shader.hpp
        src/graphics/shader.inl
        src/graphics/skybox.cpp
        src/graphics/skybox.hpp
        src/graphics/static_object.cpp
        src/graphics/static_object.hpp
        src/graphics/stb_image.h
        src/graphics/texture.cpp
        src/graphics/texture.hpp
        src/graphics/texture.inl

        src/graphics/gui/button.cpp
        src/graphics/gui/button.hpp
        src/graphics/gui/display.cpp
        src/graphics/gui/display.hpp
        src/graphics/gui/gui.cpp
        src/graphics/gui/gui.hpp
        src/graphics/gui/gui.inl
        src/graphics/gui/textfield.cpp
        src/graphics/gui/textfield.hpp
        src/graphics/gui/widget.cpp
        src/graphics/gui/widget.hpp

        src/physics/boundary.cpp
        src/physics/boundary.hpp
        src/physics/dynamic_object.cpp
        src/physics/dynamic_object.hpp
        src/physics/physics.cpp
        src/physics/physics.hpp
        src/physics/physics_object.cpp
        src/physics/physics_object.hpp

        src/utility/file.cpp
        src/utility/file.hpp
        src/utility/functional.cpp
        src/utility/functional.hpp
        src/utility/functional.inl
        src/utility/generic.cpp
        src/utility/generic.hpp
        src/utility/generic.inl
        src/utility/numeric.cpp
        src/utility/numeric.hpp
        src/utility/numeric.inl
        src/utility/string.cpp
        src/utility/string.hpp
        src/utility/time.cpp
        src/utility/time.hpp
        src/utility/time.inl
        src/graphics/sprite.cpp
        src/graphics/sprite.hpp
        src/physics/dynamic_sprite.cpp
        src/physics/dynamic_sprite.hpp
        src/graphics/animated_texture.cpp
        src/graphics/animated_texture.hpp
        src/data/scene_importer.cpp
        src/data/scene_importer.hpp
        src/data/external/tinyxml2.h
        src/data/external/tinyxml2.cpp)
target_link_libraries(engine_a OpenGL32 SDL2 SDL2_mixer SDL2_ttf SDL2main assimp)