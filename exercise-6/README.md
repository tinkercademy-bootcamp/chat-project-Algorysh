# Exercise 6

**Update this README with your answers to the questions below.**

## Adding Third Party Libraries or Source Code to Your Project

- There is a new file `src/spdlog-hello-world-main.cc`
- It uses the spdlog and fmt libraries. 
  [More info here](https://github.com/gabime/spdlog) - Fast C++ logging 
  library with various sink types and formatting options
- How do you compile this file using the `g++` CLI?
  - g++ -std=c++17 -I/usr/include/spdlog spdlog-hello-world-main.cc -lspdlog -lfmt -o spdlog
- What do you need to change in your makefile to use this library?
  - Add `LIBS = -lspdlog` to link against the library
  - Add `INC_DIRS += /usr/include/spdlog` for include path
  - Update target dependencies to include the library (add `$(LIBS)` at the end)
- How many different ways can this library be added into your project?
  - System-wide installation using package manager
  - Git submodule in your project
  - Copying source files directly into project
  - Using a package manager like Conan or vcpkg
- What are the tradeoffs in the different ways?
  - System-wide: Easy to set up, but version control is harder
  - Git submodule: Better version control, but increases repo size
  - Source files: Complete control, but harder to update
  - Package manager: Best practice, but adds complexity
- Why are there so many different ways to do it?
  - Different projects have different needs
  - Historical reasons and C++ ecosystem evolution
  - Trade-offs between ease of use and control
  
## Static Linking vs Dynamic Linking

- What are the differences between static linking and dynamic linking?
  - Static: Library code is copied into executable
  - Dynamic: Library is loaded at runtime
- What are the tradeoffs?
  - Static: Larger executable but self-contained
  - Dynamic: Smaller executable but needs library present
  - Static: Better portability
  - Dynamic: Saves system memory when multiple programs use same library
- How do you enable static linking or dynamic linking in your makefile?

## Git Clone and Building from Source

- Where is `g++` looking for the include files and library files?
- How do you find out?

## C++ Package Managers

- Why are there so many C++ package managers?
- Which one is the best one?
- Which are the most notable ways to manage the compilation of C++ projects?