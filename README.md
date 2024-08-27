# txtz

**Short string compression**

THIS IS WORK IN PROGRESS. DO NOT EXPECT ANYTHING USEFUL IN THIS REPO AT THE MOMENT.


## Prerequisites

- C++ compiler (GCC, Clang)
- CMake 3.10 or later

## Build 

### Linux

Ubuntu

```
sudo apt install g++ libboost-all-dev
```

```
git clone https://github.com/cttester/txtz.git
cd txtz
git submodule update --init
git submodule update --remote --merge
mkdir build
cd build
cmake -DCMAKE_BUILD_TYPE=Release ..
cmake --build .
```

### macOS

```
git clone https://github.com/cttester/txtz.git
cd txtz
git submodule update --init
git submodule update --remote --merge
mkdir build
cd build
cmake -DCMAKE_BUILD_TYPE=Release ..
cmake --build .
```


### Windows

In Visual Studio Developer Console:

```
git clone https://github.com/cttester/txtz.git
cd txtz
git submodule update --init
git submodule update --remote --merge
md build
cd build
cmake ..
cmake --build . --config Release
```


## Remarks

By default, Shannon-Fano encoding is used to build the binary tree. You can change that to Huffman encoding by setting `MAPBUILDING_ALGO` to `huffman` instead of `shannon-fano` when calling `cmake` to configure the project:

```
cmake -DMAPBUILDING_ALGO=huffman -DCMAKE_BUILD_TYPE=Release ..
```

TODO!!!

## License

See [LICENSE](LICENSE).
