# Greetings: CMAKE project example
This is a very simple CMAKE project example to print a greeting message 

## Dependencies
 - CMAKE (version 3.10 or higher)

## Getting Started
Add clone instructions

## Install
```bash
export cmakeDir="$PWD" # make sure you are inside the greetings directory
export buildDir="my_build"
export installDir="my_install"
mkdir "$buildDir" && cd "$buildDir"
cmake -DCMAKE_INSTALL_PREFIX="../$installDir" "$cmakeDir" # provide the correct path to the cloned repository
cmake --build . -- -j$(nproc)
cmake --install .
```

## Runing the Project


### Project Structure
In this repository the project is organised as follows:
```bash
.
├── CMakeLists.txt
├── inc
│   └── utils
│       └── tools.h
├── lib
│   └── tools.cpp
├── README.md
└── src
    └── greetings.cpp (the file with the main function)
```

Another common way to organise is:
```bash
.
├── CMakeLists.txt
├── inc
│   └── utils
│       └── tools.h
├── src 
│   └── tools.cpp
├── README.md
└── greetings.cpp (the file with the main function)
```


## Contributors
- Tamasi Kar

## Liscence
ToDo
