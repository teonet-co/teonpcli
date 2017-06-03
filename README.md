# Teonet native C++JS client server

## 1. Installation

### 1.1 Install project with submodules

    git clone git@gitlab.ksproject.org:teonet/teonpcli.git
    cd teonpcli
    git submodule update --init --recursive
    
### 1.2 Update submodules to latest version

Last version of the project used some different versions of submodules. If you 
need switch to latest versions of submodules use next git command:

    git submodule update --remote --merge

## 2. Projects description

The main Projects Goal is Creating native Web | Phonegap | Node Teonet Client which used basic C/C++ teonet client to connect to Teonet L0 server.
  &nbsp;  
  &nbsp;  
![Teonet native C++JS client server architecture](https://drive.google.com/uc?export=view&id=0B11kd5eSht0oVTlQX1pDeC05SFk)

Todo this we create complecs client with several components (see picture abow):

- JS from C/C++ Teonet client "Teonet C++JS L0 Client"; 
- JS from C/C++ Teonet connector "C++JS L0 Server";
- JS from C/C++ Teonet proxy "Teonet C++JS L0 Proxy";
- C/C++ Teonet native client Node module "Teonet C ++ Native Node L0 Client".

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

    cd teocli

### 4.2 C++JS L0 Server

### 4.3 Teonet C++JS L0 Proxy

### 4.4 Teonet C ++ Native Node L0 Client

