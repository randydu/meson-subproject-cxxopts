# CXXOPTS

Header-Only commandline parameter parser.

- URL: https://github.com/jarro2783/cxxopts
- version: v2.2.1

## Usage

- copy cxxopts.wrap to your meson-build project's subfolder "subprojects";

```
myapp/
   ├── meson.build
   ├── subprojects/
              ├── cxxopts.wrap
  
```

- in your meson.build file, imports the cxxopts dependency:

```meson
cxxopts_dep = dependency('cxxopts')

executable('myapp', dependencies: [cxxopts_dep, ...])
```

- in your source code:

```c++
#include <cxxopts.hpp>

int main(int argc, char* args[]){
    cxxopts::Options option("myapp", ...);
}
```

Done!