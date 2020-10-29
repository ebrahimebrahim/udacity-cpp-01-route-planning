# Route Planning Project

---

## Forked

This is a forked assignment, to be Ebrahim's solution to project 01 of udacity's c++ course.

### Installing IO2D on Debian

This was the only tricky part of the build instructions below.

- Ensure that cmake, make, and gcc are installed.
- Install the dependencies of IO2D: `sudo apt install libcairo2-dev libgraphicsmagick1-dev libpng-dev`
- Make sure you got all the submodules from this repo: `git submodule update --init --recursive`
- Go to `thirdparty/P0267_RefImpl` and `mkdir build; cd build;`
- Cmake only what's needed: `cmake -DIO2D_WITHOUT_TESTS=true -DIO2D_WITHOUT_SAMPLES=true ..`
- Finally, install to system: `sudo make install`

I hate the last step...
It should be possible to link the local copy of the static library that we get from just plain `make`,
and this would be better than installing to the system with `sudo make install`.
But I'm currently not understanding how to tweak `CMakeLists.txt` to get this to happen.

---

This repo contains the starter code for the Route Planning project.

<img src="map.png" width="600" height="450" />

## Cloning

When cloning this project, be sure to use the `--recurse-submodules` flag. Using HTTPS:
```
git clone https://github.com/udacity/CppND-Route-Planning-Project.git --recurse-submodules
```
or with SSH:
```
git clone git@github.com:udacity/CppND-Route-Planning-Project.git --recurse-submodules
```

## Dependencies for Running Locally
* cmake >= 3.11.3
  * All OSes: [click here for installation instructions](https://cmake.org/install/)
* make >= 4.1 (Linux, Mac), 3.81 (Windows)
  * Linux: make is installed by default on most Linux distros
  * Mac: [install Xcode command line tools to get make](https://developer.apple.com/xcode/features/)
  * Windows: [Click here for installation instructions](http://gnuwin32.sourceforge.net/packages/make.htm)
* gcc/g++ >= 7.4.0
  * Linux: gcc / g++ is installed by default on most Linux distros
  * Mac: same instructions as make - [install Xcode command line tools](https://developer.apple.com/xcode/features/)
  * Windows: recommend using [MinGW](http://www.mingw.org/)
* IO2D
  * Installation instructions for all operating systems can be found [here](https://github.com/cpp-io2d/P0267_RefImpl/blob/master/BUILDING.md)
  * This library must be built in a place where CMake `find_package` will be able to find it

## Compiling and Running

### Compiling
To compile the project, first, create a `build` directory and change to that directory:
```
mkdir build && cd build
```
From within the `build` directory, then run `cmake` and `make` as follows:
```
cmake ..
make
```
### Running
The executable will be placed in the `build` directory. From within `build`, you can run the project as follows:
```
./OSM_A_star_search
```
Or to specify a map file:
```
./OSM_A_star_search -f ../<your_osm_file.osm>
```

## Testing

The testing executable is also placed in the `build` directory. From within `build`, you can run the unit tests as follows:
```
./test
```

