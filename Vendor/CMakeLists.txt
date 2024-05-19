add_subdirectory ("SDL")
add_subdirectory ("GLEW")

target_include_directories(${CMAKE_PROJECT_NAME} PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/GLM)

add_library ("Vendor" INTERFACE)

target_link_libraries ("Vendor" INTERFACE SDL3::SDL3)
target_link_libraries ("Vendor" INTERFACE libglew_static)