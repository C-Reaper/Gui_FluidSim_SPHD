# Project README

## Overview
This project is a fluid simulation application built in C using Smoothed Particle Hydrodynamics (SPH). The main focus is on creating a real-time simulation of fluid dynamics.

## Features
- Real-time fluid simulation using SPH
- Customizable window size and resolution
- Basic control for interacting with the simulation environment

## Project Structure
```
Gui_FluidSim_SPHD/
├── build/              # .exe files produced by Main.c
├── src/                # Source code directory
│   ├── Main.c          # Entry point of the application
│   └── *.h             # Standalone header-based C-files without implementation
├── Makefile.linux      # Linux Build configuration
├── Makefile.windows    # Windows Build configuration
├── Makefile.wine       # Wine Build configuration for cross-compiling to Windows on Linux
└── Makefile.web        # Emscripten Build configuration for webassembly
```

### Prerequisites
- C/C++ Compiler and Debugger (GCC, Clang)
- Make utility
- Standard development tools
- Libraries needed:
  - X11 for window management on Linux
  - Windows API libraries for cross-compilation to Windows on Linux

## Build & Run
To build the project, navigate to the project directory and run the appropriate makefile based on your operating system:

### Linux
```bash
make -f Makefile.linux all
```

### Windows
```bash
make -f Makefile.windows all
```

### Wine (Cross-compile for Windows)
```bash
make -f Makefile.wine all
```

### WebAssembly
```bash
make -f Makefile.web all
```

For clean rebuild:
```bash
make -f Makefile.linux clean
make -f Makefile.linux all
```

Build Options
- `make -f Makefile.(os) all`: build output
- `make -f Makefile.(os) do`: build + exe output
- `make -f Makefile.(os) clean`: Remove build artifacts

To execute the built application:
```bash
make -f Makefile.linux exe
```

This README provides a basic overview of how to build and run the project on different platforms. For more detailed information, please refer to the source code and makefiles.