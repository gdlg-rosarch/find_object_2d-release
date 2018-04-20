# Script generated with Bloom
pkgdesc="ROS - The find_object_2d package"
url='http://find-object.googlecode.com'

pkgname='ros-lunar-find-object-2d'
pkgver='0.6.2_1'
pkgrel=1
arch=('any')
license=('BSD'
)

makedepends=('ros-lunar-catkin'
'ros-lunar-cv-bridge'
'ros-lunar-genmsg'
'ros-lunar-image-transport'
'ros-lunar-message-filters'
'ros-lunar-qt-gui-cpp'
'ros-lunar-roscpp'
'ros-lunar-rospy'
'ros-lunar-sensor-msgs'
'ros-lunar-std-msgs'
'ros-lunar-std-srvs'
'ros-lunar-tf'
)

depends=('ros-lunar-cv-bridge'
'ros-lunar-image-transport'
'ros-lunar-message-filters'
'ros-lunar-qt-gui-cpp'
'ros-lunar-roscpp'
'ros-lunar-rospy'
'ros-lunar-sensor-msgs'
'ros-lunar-std-msgs'
'ros-lunar-std-srvs'
'ros-lunar-tf'
)

conflicts=()
replaces=()

_dir=find_object_2d
source=()
md5sums=()

prepare() {
    cp -R $startdir/find_object_2d $srcdir/find_object_2d
}

build() {
  # Use ROS environment variables
  source /usr/share/ros-build-tools/clear-ros-env.sh
  [ -f /opt/ros/lunar/setup.bash ] && source /opt/ros/lunar/setup.bash

  # Create build directory
  [ -d ${srcdir}/build ] || mkdir ${srcdir}/build
  cd ${srcdir}/build

  # Fix Python2/Python3 conflicts
  /usr/share/ros-build-tools/fix-python-scripts.sh -v 2 ${srcdir}/${_dir}

  # Build project
  cmake ${srcdir}/${_dir} \
        -DCMAKE_BUILD_TYPE=Release \
        -DCATKIN_BUILD_BINARY_PACKAGE=ON \
        -DCMAKE_INSTALL_PREFIX=/opt/ros/lunar \
        -DPYTHON_EXECUTABLE=/usr/bin/python2 \
        -DPYTHON_INCLUDE_DIR=/usr/include/python2.7 \
        -DPYTHON_LIBRARY=/usr/lib/libpython2.7.so \
        -DPYTHON_BASENAME=-python2.7 \
        -DSETUPTOOLS_DEB_LAYOUT=OFF
  make
}

package() {
  cd "${srcdir}/build"
  make DESTDIR="${pkgdir}/" install
}

