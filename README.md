#external-libclang
libclang binaries and header files

##LIBCLANG 3.9.0
[http://clang.llvm.org/](http://clang.llvm.org/)  
  
**BUILD ENVIRONMENT**  
* Visual Studio 2015  
* [CMake](https://cmake.org/download/)  
* [Python](https://www.python.org/downloads/)  
  
**SOURCE CODE**  
Download [LLVM 3.9.0](http://llvm.org/releases/3.9.0/llvm-3.9.0.src.tar.xz)  
Download [Clang 3.9.0](http://llvm.org/releases/3.9.0/cfe-3.9.0.src.tar.xz)  
Extract llvm-3.9.0.src.tar.xz {somewhere}\llvm-3.9.0.src  
Extract cfe-3.9.0.src.tar.xz into {somewhere}\llvm-3.9.0.src\tools\cfe-3.9.0.src  
Rename cfe-3.9.0.src directory to clang  
  
**HEADERS**  
{somewhere}\llvm-3.9.0.src\tools\clang\include\clang-c  
  
**BUILD (Win32)**  
Open Developer Command Prompt for Visual Studio  
```
cd {somewhere}
md llvm-3.9.0-x86
cd llvm-3.9.0-x86
cmake -G "Visual Studio 14" ..\llvm-3.9.0.src\ -DLLVM_TARGETS_TO_BUILD=X86
devenv LLVM.sln /Build "Release|Win32" /project libclang
```
Get libclang.lib from {somewhere}\llvm-3.9.0-x86\Release\lib  
Get libclang.dll from {somewhere}\llvm-3.9.0-x86\Release\bin  
  
**BUILD (x64)**  
Open Developer Command Prompt for Visual Studio  
```
cd {somewhere}
md llvm-3.9.0-x64
cd llvm-3.9.0-x64
cmake -G "Visual Studio 14 Win64" ..\llvm-3.9.0.src\ -DLLVM_TARGETS_TO_BUILD=X86
devenv LLVM.sln /Build "Release|x64" /project libclang
```
Get libclang.lib from {somewhere}\llvm-3.9.0-x64\Release\lib  
Get libclang.dll from {somewhere}\llvm-3.9.0-x64\Release\bin  


