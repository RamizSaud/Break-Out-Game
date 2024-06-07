add_library(shader shader.cpp)
target_include_directories(shader PUBLIC ../include)
target_link_libraries(shader PRIVATE ${OPENGL_LIBRARIES} glfw glad glm)

add_library(stb_image stb_image.cpp)
target_include_directories(stb_image PUBLIC ../include)
target_link_libraries(stb_image PRIVATE ${OPENGL_LIBRARIES} glfw glad glm)

add_library(texture texture.cpp)
target_include_directories(texture PUBLIC ../include)
target_link_libraries(texture PRIVATE ${OPENGL_LIBRARIES} glfw glad glm shader)

add_library(resource_manager resource_manager.cpp)
target_include_directories(resource_manager PUBLIC ../include)
target_link_libraries(resource_manager PRIVATE ${OPENGL_LIBRARIES} glfw glad glm shader texture stb_image)