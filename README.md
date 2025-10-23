# cgal-vcpkg-windows Project

This project demonstrates how to use vcpkg to manage dependencies for a C++ project that utilizes the CGAL library. 

## Prerequisites

- Windows operating system
- Git
- CMake
- vcpkg

## Setup Instructions

1. **Clone the Repository**

   Clone this repository to your local machine using the following command:

   ```
   git clone https://github.com/yourusername/cgal-vcpkg-windows.git
   ```

2. **Install vcpkg**

   If you haven't installed vcpkg yet, you can do so by following these steps:

   ```bash
   git clone https://github.com/microsoft/vcpkg.git
   cd vcpkg
   ./bootstrap-vcpkg.bat
   ```

   Make sure to add vcpkg to your system's PATH.

3. **Install Dependencies**

   Navigate to the project directory and run the following command to install the required dependencies:

   ```bash
   vcpkg install
   ```

4. **Build the Project**

   Use CMake to configure and build the project:

   ```bash
   mkdir build
   cd build
   cmake .. -DCMAKE_TOOLCHAIN_FILE=[path to vcpkg]/scripts/buildsystems/vcpkg.cmake
   cmake --build .
   ```

5. **Run the Program**

   After building, you can run the program:

   ```bash
   ./your_executable_name
   ```

## Project Structure

- `.github/workflows/windows-vcpkg-cgal.yml`: GitHub Action workflow for building the project on Windows.
- `vcpkg.json`: Specifies the dependencies for the project.
- `CMakeLists.txt`: CMake configuration file for the project.
- `src/main.cpp`: Contains the "Hello World" C++ program.
- `.gitignore`: Specifies files and directories to ignore in Git.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.