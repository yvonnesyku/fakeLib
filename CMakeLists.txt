# Set the minimum required CMake version
cmake_minimum_required(VERSION 3.20)

# Set the project name
project(FakeLib)

# Set the library name
set(LIBRARY_NAME FakeLib)

# Add the library source files
set(SOURCES
    src/file1.cpp
)

# Add the library header files
set(HEADERS
    file1.hpp
)

# Create the library target
add_library(${LIBRARY_NAME} ${SOURCES} ${HEADERS})

# Set the include directories
target_include_directories(${LIBRARY_NAME} PUBLIC include)

# Set any additional compiler flags or options
# target_compile_options(${LIBRARY_NAME} PRIVATE ...)

# Set any additional linker flags or options
# target_link_options(${LIBRARY_NAME} PRIVATE ...)

# Optionally, add any dependencies
# target_link_libraries(${LIBRARY_NAME} PUBLIC ...)

# Optionally, install the library
# install(TARGETS ${LIBRARY_NAME} DESTINATION lib)
# install(FILES ${HEADERS} DESTINATION include/mylibrary)
