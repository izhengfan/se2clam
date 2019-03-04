se2clam
---
SE(2)-Constrained Localization and Mapping by Fusing Odometry and Vision

### Related Publication

- Fan Zheng, Hengbo Tang, Yun-Hui Liu. "Odometry-Vision-Based Ground Vehicle Motion Estimation With SE(2)-Constrained SE(3) Poses". _IEEE Transactions on Cybernetics_, 2018


### Dependencies

- ROS (tested on Kinetic/Melodic)

- OpenCV 2.4.x / 3.1 above

- g2o ([2016 version](https://github.com/RainerKuemmerle/g2o/releases/tag/20160424_git))

### Build

Build this project as a ROS package

### Demo

1. Download [DatasetRoom.zip](https://mycuhk-my.sharepoint.com/:u:/g/personal/1155051778_link_cuhk_edu_hk/Ef4NuXvLZI1JhfljH9LkNxUB5xrDrCOrRnxwztO5bGKlew?e=U4aind), and extract it. In a terminal, `cd` into `DatasetRoom/`.

   We prepare two packages of odometry measurement data, one is more accurate (`odo_raw_accu.txt`), the other less accurate (`odo_raw_roug.txt`). To use either one of them, copy it to `odo_raw.txt` in `DatasetRoom/`.

2. Download [ORBvoc.bin](http://files.git.oschina.net/group1/M00/00/7A/ZxV3cFeI9XmAby8AAqT02a7stTI369.bin?token=cfa452605a820832918e620075c2ae9f&ts=1551679978&attname=ORBvoc.bin).

3. Run rviz:

   ```
   roscd se2clam
   rosrun rviz rviz -d rviz.rviz
   ```

4. Run se2clam:
   
   ```
   rosrun se2clam test_vn PATH_TO_DatasetRoom PATH_TO_ORBvoc.bin
   ```

   ![result in rviz](https://images.gitee.com/uploads/images/2019/0304/153637_976bd726_874043.jpeg)
   
   
### Related Project

[izhengfan/se2lam](https://github.com/izhengfan/se2lam)

### License 

[MIT](LICENSE)

