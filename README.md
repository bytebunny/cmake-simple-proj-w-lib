# CMake example of a project with libraries

An example of how a project structure can be organised when we have a target that uses 3rd party library that we can build from source.

## Usage

1. Build and run the project:

    ```
    cmake -S . -B build
    cmake --build build
    build/cmake-simple-proj-w-lib
    ```

1. Verify the expected output: `/// my_lib::add_one( 2 ) returned 3`
