cmake_minimum_required(VERSION 3.8)
project(data_tum)

find_package(ament_cmake REQUIRED)

set(freiburg2_pioneer_360   https://vision.in.tum.de/rgbd/dataset/freiburg2/rgbd_dataset_freiburg2_pioneer_360.tgz)
set(freiburg2_pioneer_slam  https://vision.in.tum.de/rgbd/dataset/freiburg2/rgbd_dataset_freiburg2_pioneer_slam.tgz)
set(freiburg2_pioneer_slam2 https://vision.in.tum.de/rgbd/dataset/freiburg2/rgbd_dataset_freiburg2_pioneer_slam2.tgz)
set(freiburg2_pioneer_slam3 https://vision.in.tum.de/rgbd/dataset/freiburg2/rgbd_dataset_freiburg2_pioneer_slam3.tgz)


if(NOT DEFINED TUM_DATASET)
  set(TUM_DATASET freiburg2_pioneer_360 CACHE STRING "TUM Dataset")
endif()

set(TUM_DATASET_URL ${${TUM_DATASET}})
include(FetchContent)
FetchContent_Declare(
  ${TUM_DATASET}
  URL ${TUM_DATASET_URL}
  SOURCE_DIR ${CMAKE_CURRENT_BINARY_DIR}/${TUM_DATASET}
)
FetchContent_MakeAvailable(${TUM_DATASET})



if(BUILD_TESTING)
  find_package(ament_lint_auto REQUIRED)
  # the following line skips the linter which checks for copyrights
  # comment the line when a copyright and license is added to all source files
  set(ament_cmake_copyright_FOUND TRUE)
  # the following line skips cpplint (only works in a git repo)
  # comment the line when this package is in a git repo and when
  # a copyright and license is added to all source files
  set(ament_cmake_cpplint_FOUND TRUE)
  ament_lint_auto_find_test_dependencies()
endif()

ament_package()
