
vcpkg install --triplet x64-mingw-dynamic


## Windows compilation

g++ .\src\main.cpp -o ./builds/build.exe -I.\vcpkg_installed\x64-mingw-dynamic\include\ -L.\vcpkg_installed\x64-mingw-dynamic\lib\ -lwinmm -lgdi32 -lglad -lglfw3dll

## Macos compilation

g++ -I./vcpkg_installed/x64-osx/include -L./vcpkg_installed/x64-osx/lib -lraylib -lglfw3 -framework CoreVideo -framework IOKit -framework Cocoa -framework GLUT -framework OpenGL ./src/main.cpp -o ./builds/Build.exe -std=gnu++17  

## Linux compilation

g++ ./src/main.cpp -I./vcpkg_installed/x64-linux/include -L./vcpkg_installed/x64-linux/lib -lraylib -lglfw3 -lpthread -ldl -o ./builds/Build.exe