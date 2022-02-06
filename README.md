## TUM Dataset Downloader

This ROS2 package downloads the specified Tar from [TUM Dataset](https://vision.in.tum.de/data/datasets/rgbd-dataset/download).

### Usage

```
colcon build --merge-install --packages-select data_tum --cmake-args -DTUM_DATASET=<Tar>
```
Refer to the table bellow for tar names. By default freiburg2_pioneer_360 will be downloaded.
```
colcon build --merge-install --packages-select data_tum
```

### Bags

| Bag                     | Link                                                                                     |
|-------------------------|------------------------------------------------------------------------------------------|
| freiburg2_pioneer_360   | https://vision.in.tum.de/rgbd/dataset/freiburg2/rgbd_dataset_freiburg2_pioneer_360.bag   |
| freiburg2_pioneer_slam  | https://vision.in.tum.de/rgbd/dataset/freiburg2/rgbd_dataset_freiburg2_pioneer_slam.bag  |
| freiburg2_pioneer_slam2 | https://vision.in.tum.de/rgbd/dataset/freiburg2/rgbd_dataset_freiburg2_pioneer_slam2.bag |
| freiburg2_pioneer_slam3 | https://vision.in.tum.de/rgbd/dataset/freiburg2/rgbd_dataset_freiburg2_pioneer_slam3.bag |

### Tars

| Tar                     | Link                                                                                     |
|-------------------------|------------------------------------------------------------------------------------------|
| freiburg2_pioneer_360   | https://vision.in.tum.de/rgbd/dataset/freiburg2/rgbd_dataset_freiburg2_pioneer_360.tgz   |
| freiburg2_pioneer_slam  | https://vision.in.tum.de/rgbd/dataset/freiburg2/rgbd_dataset_freiburg2_pioneer_slam.tgz  |
| freiburg2_pioneer_slam2 | https://vision.in.tum.de/rgbd/dataset/freiburg2/rgbd_dataset_freiburg2_pioneer_slam2.tgz |
| freiburg2_pioneer_slam3 | https://vision.in.tum.de/rgbd/dataset/freiburg2/rgbd_dataset_freiburg2_pioneer_slam3.tgz |
