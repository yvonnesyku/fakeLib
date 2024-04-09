# Set the minimum required CMake version
cmake_minimum_required(VERSION 3.20)

# Create the library target
add_library(FakeLib STATIC "")

target_sources(FakeLib PRIVATE src/file1.cpp PUBLIC file1.hpp)

target_include_directories(FakeLib PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

install(FILES file1.hpp DESTINATION ${CMAKE_INSTALL_INCLUDEDIR}/${PROJECT_NAME})

install(TARGETS FakeLib
ARCHIVE DESTINATION ${CMAKE_INSTALL_LIBDIR}
RUNTIME DESTINATION ${CMAKE_INSTALL_LIBDIR}
)


