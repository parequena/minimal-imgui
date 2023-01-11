# minimal-imgui
Minimal Imgui Code to compile SDL/OpenGL3 example</br>
The purpose of this repository is to use it as a [git submodule](https://git-scm.com/book/en/v2/Git-Tools-Submodules) on a other repo. </br>
Feel free to modify, add, fix any `CMakeLists.txt` related code/instructions using [Github Issues from this repo](https://github.com/parequena/minimal-imgui/pulls) and I'll try to add them however I can.

## Compilation
- Clone this repo `git clone https://github.com/parequena/minimal-imgui.git`
- Create output folder: `mkdir build && cd build`
- Generate project `cmake .. -DSTATIC=ON` ON=Static_lib, OFF/Empty=Shared_lib
- This project is always generated in `Release` mode, to change that, you must modify our `CMakeLists.txt`
- Compile our library `cmake --build .`

## Dependencies

- OpenGL
- Glew
- [SDL2](https://www.libsdl.org/)

## Reproduce steps
- Go to [ImGUI](https://github.com/ocornut/imgui)
- Go to docking branch (11/01/2023)
- Copy [this code](https://github.com/ocornut/imgui/blob/docking/examples/example_sdl_opengl3/main.cpp) from Imgui Examples (SDL/OpenGL3).
- Get all dependences from that code.
- Move all `.h` files into `include` folder.
- Move all `.cpp` files into `src` folder.
- Create an `CMakeLists.txt`

## About / Reach me
- [Twitter](https://twitter.com/conPdePABLO) In Spanish!
- [LinkedIn](https://www.linkedin.com/in/parequena/)
- Email: parequena8@gmail.com
