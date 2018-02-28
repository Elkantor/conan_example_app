# conan_example_app
Example repository to build a project by using the conan (cmake under the hood) C++ package manager.

To test this project, you need to install conan and the msvs tools on windows (or MinGW to have access to the gcc compiler, because conan will always find your C++ compiler by himself).
The best way to install conan is to use tools like chocolatey on windows, for example.

Once you have conan installed, you can type the following command: 

```shell
conan install . --install-folder build
```

This will create the template for building this project, based on the CMakeLists.txt (located in the ether/ directory).
This command creates a new folder, at the root of this git repository, named "build".

You can now build this project with conan:
```shell
conan build . --build-folder build
```

This will create the solution for your OS, depending of the build generator used by cmake. By default, on windows, if you have Visual Studio installed, it will take the msvs generator.
So that will create a sln solution for Visual Studio, in your /build folder, and compile the code to an executable file (again, on windows), in the /build/bin folder, as we expect.
