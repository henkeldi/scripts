#!/bin/bash
VERSION=$1
#VERSION=4.3.0
mkdir -p $HOME/src
cd $HOME/src
wget https://github.com/opencv/opencv/archive/$VERSION.tar.gz
tar xvf $VERSION.tar.gz
rm $VERSION.tar.gz
wget https://github.com/opencv/opencv_contrib/archive/$VERSION.tar.gz
tar xvf $VERSION.tar.gz
rm $VERSION.tar.gz
cd opencv-$VERSION
mkdir build
cd build
cmake -DOPENCV_EXTRA_MODULES_PATH=$HOME/src/opencv_contrib-$VERSION/modules\
      -DCMAKE_BUILD_TYPE=RELEASE -DBUILD_EXAMPLES=OFF -DBUILD_DOCS=OFF\
      -DBUILD_PERF_TESTS=OFF -DBUILD_TESTS=OFF -DENABLE_PRECOMPILED_HEADERS=OFF ..
make -j8
