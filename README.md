# Teonet native C++JS client server

## 1. Installation

## 2. Projects description

The main Projects Goal is Creating native Web | Phonegap | Node Teonet Client which used basic C/C++ teonet client to connect to Teonet L0 server. 

Todo this we create complecs client with several components (see picture below):

- JS from C/C++ Teonet client "Teonet C++JS L0 Client"; 
- JS from C/C++ Teonet connector "C++JS L0 Server";
- JS from C/C++ Teonet proxy "Teonet C++JS L0 Proxy";
- C/C++ Teonet native client Node module "Teonet C ++ Native Node L0 Client".
&nbsp;    
&nbsp;

![Teonet native C++JS client server architecture](https://lh3.googleusercontent.com/YySiMzS01xIax5i3XaKdjciThE146MoT9eLwNbh4voDhd5KP6j_VAM-a_yJlS2tEjmUYTkLnVMVXymY=w1356-h657)

## 3. C++ to JS convert techologes used in this project

To create JS from C/C++ we uses [Emscripten](http://kripken.github.io/emscripten-site/#) to 
Compile our existing projects written in C or C++ and run them on all modern browsers. 
[Emscripten](http://kripken.github.io/emscripten-site/#) is an LLVM-based project 
that compiles C and C++ into highly-optimizable JavaScript in asm.js format. 
This lets us run C and C++ on the web at near-native speed, without plugins.

To execute Emscripten on different platforms without setup we use docker image from [trzeci](https://hub.docker.com/r/trzeci/emscripten/):

To execute emcc comiller from container use next command:

    docker run --rm -v $(pwd):/src trzeci/emscripten:sdk-tag-1.37.3-64bit emcc
    
To compile single C/C++ file to JS it could be called like:

    docker run --rm -v $(pwd):/src trzeci/emscripten:sdk-tag-1.37.3-64bit emcc helloworld.cpp -o helloworld.js


## 4. Projects components description

### 4.1 Teonet C++JS L0 Client

### 4.2 C++JS L0 Server

### 4.3 Teonet C++JS L0 Proxy

### 4.4 Teonet C ++ Native Node L0 Client

