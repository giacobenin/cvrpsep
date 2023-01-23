# cvrpsep

This is my "fork" of the CVRPSEP package for separation algorithms for Capacitated Vehicle Routing Problem which is hosted at https://econ.au.dk/research/researcher-websites/jens-lysgaard/cvrpsep/.

In the initial commit, the only change is to rename the source code to all lower case convention (rename.sh). The original code was mixed and caused some issues on some hosts. Otherwise, the initial commit is a copy of the original source. Subsequent commits will include contributed fixes and improvements.

## Build

### Make

A `Makefile` for Linux and MacOSX is provided. g++ is required. From the cvrsep folder:

```
make
```

### CMake

Alternatively, CMake can be used to build on Linux, OSX, and Windows (CMake can be used to generate a Visual Studio solution).

From the cvrsep folder:
```
/cmake --build /cvrpsep/cmake-build-debug --target all -j 3
```

On Windows the CMake project can be built [using Visual Studio](https://learn.microsoft.com/en-us/cpp/build/cmake-projects-in-visual-studio?view=msvc-170) directly, or CMake can be used to generated Visual Studio solutions.
