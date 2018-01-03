Conan Boost Example
===================

Example of Boost.Asio using Conan

Files needed (included in this repo)
------------------------------------

- Source code: *async_tcp_echo_server.cpp*
- Build file: *CMakeListst.txt*
- Dependency file: *conanfile.txt*

Binary remotes
--------------

This projects uses conan packages from Bincrafters repository.
To add this remote to you Conan client do this:

``$ conan remote add bincrafters https://api.bintray.com/conan/bincrafters/public-conan``

Build steps
-----------

Retrieve your dependencies with Conan:

```
$ cd conan_boost_example
$ conan install .
# Looks for dependencies, downloads packages and generates conanbuildinfo.cmake with variables
```

Configure and build your project with CMake normally (here with Visual Studio):

```
$ cmake configure . -G "Visual Studio 15 2017 Win64"
$ cmake --build . --config Release
# Compiles target in bin/async_tcp_echo_server.exe
```
