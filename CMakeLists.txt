project(z2engine)

cmake_minimum_required(VERSION 2.8)

# Find packages

# Project source code
set(SOURCES
)

# Inlucde directories for libraries
set(INCLUDE_DIRS
)

# Libraries for linking
set(LIBRARIES
)

# Configuration
include_directories(include/)
include_directories(${INCLUDE_DIRS})

# Enable 11 C++ standard
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

# Compiling
add_library(${PROJECT_NAME} SHARED ${SOURCES})
add_library(${PROJECT_NAME}_static STATIC ${SOURCES})

# Linking
target_link_libraries(${PROJECT_NAME} ${LIBRARIES})

# Install
install(TARGETS ${PROJECT_NAME} DESTINATION lib)
install(DIRECTORY include/engine/ DESTINATION include/z2engine)
