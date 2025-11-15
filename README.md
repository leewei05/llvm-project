# LLVM Bamboo backend

```sh
mkdir build && cd build
cmake -G Ninja ../llvm \
  -DLLVM_ENABLE_PROJECTS="llvm" \
  -DCMAKE_BUILD_TYPE=Debug \
  -DLLVM_EXPERIMENTAL_TARGETS_TO_BUILD="Bamboo" \
  -DLLVM_ENABLE_ASSERTIONS=ON
```