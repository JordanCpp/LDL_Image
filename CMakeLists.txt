project(LDL_Image)

if (MSVC)
    add_definitions(-D_CRT_SECURE_NO_WARNINGS)
    add_definitions(-D_CRT_NONSTDC_NO_DEPRECATE)  
endif()

add_definitions(-DLDL_IMAGE_SHARED)

include_directories("include")
add_library(${CMAKE_PROJECT_NAME} SHARED "source/LDL_Image.cpp")

add_executable(test "test.cpp")
target_link_libraries(test ${CMAKE_PROJECT_NAME})
