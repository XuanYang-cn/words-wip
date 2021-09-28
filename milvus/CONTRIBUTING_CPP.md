# How to contribute to CPP?

## How to build from source?

See [Building Milvus on a local OS/shell environment](DEVELOPMENT.md#building-milvus-on-a-local-osshell-environment), make sure your environment meets the hardware and software requirements.

Building CPP code from source is slightly different with Golang. Most of our CPP codes are lied in directory `milvus/internal/core`, so most developments on CPP are based on this directory.

Build from source using  `build.sh` script:

```shell
milvus/internal/core$ ./build.sh -u -t Debug -o cmake-build-debug
```

- `-u`: Build unit tests
- `-t Debug`:  Build debug version
- `-o cmake-build-debug`: Write build files into `cmake-build-debug` directory.

Use `./build.sh -h` to know the more detailed usages of `build.sh` .

## Coding style guidelines

The coding style used in CPP of Milvus generally follow [Google C++ Style Guide](https://google.github.io/styleguide/cppguide.html).
And we made the following changes based on the guide:

-   4 spaces for indentation
-   Adopt `.cpp` file extension instead of `.cc` extension
-   120-character line length
-   Camel-Cased file names

### Format code

Install clang-format

```shell
$ sudo apt install clang-format-10
```

Check code style

```shell
# Run clang_format at milvus/internal/core/
milvus/internal/core$ ./run_clang_format .
# Or run cpplint, clang_format, and liscense check all together in milvus/
milvus$ make cppchek
```

## How to run unit tests?

Run unit tests of CPP in `milvus/`

```shell
milvus$ make test-cpp
```

Todo: run unit tests with code coverage, we don't have this check yet.
