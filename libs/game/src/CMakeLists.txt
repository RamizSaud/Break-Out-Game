# add_library(game game.cpp)
# target_include_directories(game PUBLIC ../include)
# target_link_libraries(game PRIVATE ${OPENGL_LIBRARIES} glfw glad glm resource_manager sprite shader texture)

# add_library(sprite sprite_renderer.cpp)
# target_include_directories(sprite PUBLIC ../include)
# target_link_libraries(sprite PRIVATE ${OPENGL_LIBRARIES} glfw glad glm texture shader resource_manager)

# add_library(game_object game_object.cpp)
# target_include_directories(game_object PUBLIC ../include)
# target_link_libraries(game_object PRIVATE ${OPENGL_LIBRARIES} glfw glad glm texture shader resource_manager sprite)

# add_library(game_level game_level.cpp)
# target_include_directories(game_level PUBLIC ../include)
# target_link_libraries(game_level PRIVATE ${OPENGL_LIBRARIES} glfw glad glm texture shader resource_manager sprite game_object)

# add_library(ball_object ball_object.cpp)
# target_include_directories(ball_object PUBLIC ../include)
# target_link_libraries(ball_object PRIVATE ${OPENGL_LIBRARIES} glfw glad glm texture shader resource_manager sprite game_object)

# add_library(ball_object_collisions ball_object_collisions.cpp)
# target_include_directories(ball_object_collisions PUBLIC ../include)
# target_link_libraries(ball_object_collisions PRIVATE ${OPENGL_LIBRARIES} glfw glad glm texture shader resource_manager sprite game_object)

add_library(game game.cpp sprite_renderer.cpp game_object.cpp game_level.cpp ball_object.cpp ball_object_collisions.cpp)
target_include_directories(game PUBLIC ../include)
target_link_libraries(game PRIVATE ${OPENGL_LIBRARIES} glfw glad glm shader texture resource_manager stb_image)