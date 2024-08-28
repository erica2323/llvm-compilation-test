# llvm-compilation-test
# Steps Completed for LLVM and C++ Compilation

1. Cloned the LLVM repository:
   Command: `git clone https://github.com/llvm/llvm-project.git`

2. Built LLVM:
   Commands:
   ```
   cd llvm-project
   mkdir -p build
   cd build
   cmake -DCMAKE_BUILD_TYPE=Release -DLLVM_ENABLE_PROJECTS="clang;clang-tools-extra" ../llvm
   make -j4
   sudo make install
   ```

3. Compiled and ran "Hello, World!" using Clang:
   Commands:
   ```
   cd ~/Desktop
   echo '#include <iostream>' > hello.cpp
   echo 'int main() { std::cout << "Hello, World!"; return 0; }' >> hello.cpp
   clang++ -o hello hello.cpp
   ./hello
   ```
   Output:
   ```
   Hello, World!
   ```
