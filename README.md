# Data2Array
Tool to pack external files into an array

### Usage
```
Usage: Data2Array <opts> -o <output file> -i <input file(s)>

    <opts>:
       -b - generate array for the unsigned char datatype [0, 255]
       -f - generate for ASCII characters only.
```

### Usage for CMake
```
set(CMAKE_MODULE_PATH ${CMAKE_SOURCE_DIR}/CMake)
include(Data2Array)

add_templates(
    some_file_name.h 
    test.txt)

set(SRCFILES 
    some_file_name.h
    main.cpp
)
add_executable(SomeTarget ${SRCFILES})

```


### Output
```
const unsigned char TEST[110]={
    0x23, 0x69, 0x6E, 0x63, 0x6C, 0x75, 0x64, 0x65, 0x20, 0x22, 0x73, 0x74, 0x64, 0x69, 0x6F, 0x2E, 
    0x68, 0x22, 0x0D, 0x0A, 0x0D, 0x0A, 0x69, 0x6E, 0x74, 0x20, 0x6D, 0x61, 0x69, 0x6E, 0x28, 0x69, 
    0x6E, 0x74, 0x20, 0x61, 0x72, 0x63, 0x67, 0x2C, 0x20, 0x63, 0x68, 0x61, 0x72, 0x20, 0x2A, 0x2A, 
    0x61, 0x72, 0x67, 0x76, 0x29, 0x0D, 0x0A, 0x7B, 0x0D, 0x0A, 0x20, 0x20, 0x20, 0x20, 0x70, 0x72, 
    0x69, 0x6E, 0x74, 0x66, 0x28, 0x22, 0x48, 0x65, 0x6C, 0x6C, 0x6F, 0x20, 0x77, 0x6F, 0x72, 0x6C, 
    0x64, 0x5C, 0x6E, 0x22, 0x29, 0x3B, 0x0D, 0x0A, 0x20, 0x20, 0x20, 0x20, 0x72, 0x65, 0x74, 0x75, 
    0x72, 0x6E, 0x20, 0x30, 0x3B, 0x0D, 0x0A, 0x7D, 0x0D, 0x0A, 0x0D, 0x0A, 0x00
};// TEST2
const unsigned int TEST_SIZE=109;

```
