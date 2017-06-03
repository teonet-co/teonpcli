# Teonet native C++JS client server

## Project description

The main Project Goal is Creating native Web | Phonegap | Node Teonet Client which used basic C/C++ teonet client to connect to Teonet L0 server. 

Todo this we create complecs client with several components (see picture below):

- JS from C/C++ Teonet client "Teonet C++JS L0 Client"; 
- JS from C/C++ Teonet connector "C++JS L0 Server";
- JS from C/C++ Teonet proxy "Teonet C++JS L0 Proxy";
- C/C++ Teonet native client Node module "Teonet C ++ Native Node L0 Client".
&nbsp;    
&nbsp;

![Teonet native C++JS client server architecture](https://lh5.googleusercontent.com/n0VK-QLgILYtGXWbGvOaisN_y-fQdVM9THYtp6S7xpmZZO8pjXmWCLprvvm-qed7DIrGy81hWai_AWA=w1356-h657)

## Basic techologes used in project

To create JS from C/C++ we uses [Emscripten](http://kripken.github.io/emscripten-site/#) to Compile our existing projects written in C or C++ and run them on all modern browsers.

Emscripten is an LLVM-based project that compiles C and C++ into highly-optimizable JavaScript in asm.js format. This lets you run C and C++ on the web at near-native speed, without plugins.