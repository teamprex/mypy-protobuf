# PrestoLabs customized mypy-protobuf
mypy-protobuf: Generate mypy stub files from protobuf specs

- Original: `origin-main` branch
- Customized parts: https://github.com/prestolabs/mypy-protobuf/commit/5e271cd8f48ab4e4ed1d5f1c1e7e20ad35ca7f8c

## Installation

The plugin can be installed with
```
pip3 install git+git://github.com/prestolabs/mypy-protobuf@main
```
In order to run mypy on the generated code, you'll need to install
```
pip3 install mypy>=0.910 types-protobuf>=0.1.14
```

## Usage

On posix, protoc-gen-mypy is installed to python's executable bin. Assuming that's
on your $PATH, you can run
```
protoc --python_out=output/location --mypy_out=output/location
```
Alternately, you can explicitly provide the path:
```
protoc --plugin=protoc-gen-mypy=path/to/protoc-gen-mypy --python_out=output/location --mypy_out=output/location
```
Check the version number with
```
> protoc-gen-mypy --version
```

Licence etc.
------------

[![license](https://img.shields.io/github/license/dropbox/mypy-protobuf)](https://github.com/dropbox/mypy-protobuf/blob/main/LICENSE)
1. License: Apache 2.0.
2. Copyright attribution: Copyright (c) 2017 Dropbox, Inc.
3. External contributions to the project should be subject to
   Dropbox's Contributor License Agreement (CLA):
   https://opensource.dropbox.com/cla/
