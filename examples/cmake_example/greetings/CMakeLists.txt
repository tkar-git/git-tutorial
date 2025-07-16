# Specify the minimum required version of CMake
cmake_minimum_required(VERSION 3.10)

# Define the project name
project(Greetings)

# Set the output directory for the compiled executable
# ${CMAKE_BINARY_DIR} is the build directory (e.g., build/)
# ../run makes it one level up and into the 'run' directory
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/../run)

# Add the 'inc' directory to the list of paths for header file lookup
include_directories(inc)

# Create a static library named 'utils' from the source file 'lib/tools.cpp'
# STATIC means the library will be compiled into the executable at link time
add_library(utils STATIC
    lib/tools.cpp
)

# Create an executable named 'greetings' from the source file 'src/greetings.cpp'
add_executable(greetings
    src/greetings.cpp
)

# Link the 'utils' library to the 'greetings' executable
# PRIVATE means 'utils' is only used internally by 'greetings'
target_link_libraries(greetings PRIVATE utils)
