### cmake-gtest-example
Simple example how to structure C++ source code with gtest.

* Initially inspired from this blog: http://kaizou.org/2014/11/gtest-cmake/.
* The related code can be found here: https://github.com/kaizouman/gtest-cmake-example .

### How to build
* Clone repository
* mkdir build
* cd build
* cmake ../src
* make -j4

### Run tests
* ./test/main/runtests

### How to measure coverage
* install lcov with sudo apt install lcov
* Clone repository
* mkdir build
* cd build
* cmake -DCMAKE_BUILD_TYPE=Debug ../src
* make -j4
* make coverage
