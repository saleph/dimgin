# dimgin
4d game engine

```
sudo apt install pip cmake build-essential
export CONAN_VENV='~/.python/venv/conan'
python -m venv ${CONAN_VENV}
export PATH=${CONAN_VENV}/bin:$PATH
sudo pip install conan

conan install . --output-folder=build --build=missing
cmake -S . -DCMAKE_TOOLCHAIN_FILE=conan_toolchain.cmake -DCMAKE_BUILD_TYPE=Release -B build
cmake --build build
./build/tests
```