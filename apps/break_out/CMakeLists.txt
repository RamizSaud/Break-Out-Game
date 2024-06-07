find_package(OpenGL REQUIRED)
add_executable(output program.cpp)
# target_link_libraries(output PRIVATE ${OPENGL_LIBRARIES} glfw glad glm shader stb_image game resource_manager sprite game_object game_level ball_object ball_object_collisions)
target_link_libraries(output PRIVATE ${OPENGL_LIBRARIES} glfw glad glm shader stb_image game)

file(COPY "${CMAKE_CURRENT_SOURCE_DIR}/shaders" DESTINATION "${CMAKE_CURRENT_BINARY_DIR}")
file(COPY "${CMAKE_CURRENT_SOURCE_DIR}/textures" DESTINATION "${CMAKE_CURRENT_BINARY_DIR}")
file(COPY "${CMAKE_CURRENT_SOURCE_DIR}/levels" DESTINATION "${CMAKE_CURRENT_BINARY_DIR}")