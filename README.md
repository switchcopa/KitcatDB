# KitcatDB

## What is KitcatDB? 

KitcatDB is a lightweight database that stores key-value pairs in normal .txt files.

## License 

MIT License

Copyright (c) 2025 Rayane

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

## Usage 

### Welcome to KitcatDB. 

KitcatDB serves to be the stupidest way to store key-value data into .txt files.
This acts as a project to practice and visualize a way how key-value data is
stored, deleted and retrieved.

For documentation on the API go to [API](https://github.com/switchcopa/KitcatDB/blob/main/docs/api.md?plain=1)

### Build 

#### Copying the source 

To build, use and modify the code, clone the repository into your local machine.

```
git clone https://github.com/switchcopa/KitcatDB
```

#### CMake

With CMake 3.10 or later are supported, make a `build` directory and run CMake inside it.

```
mkdir build 
cd build 
cmake ..
```

This will create a Makefile and a bunch of other files. You can then compile it:

```
make
```

### Running

After building, you can run the program directly from the `build/` folder:

```
./kitcat-db
```

## Notes 

KitcatDB is meant for learning and experimentation, not for production use.

All data is stored in plain text files, so please don't store sensitive data here.

This project is intentionally simple to demonstrate the basic concepts of a runtime key-value database.
