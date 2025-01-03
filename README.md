# Loc_Dataset
本数据集用于A2RL定位测试。<br>
This dataset is used for localization testing.<br>



## 场景划分 Scene type
| Scene | Time | Velocity | LiDAR |
|:-----------|------------:|:------------:|------------:|
| slow_long_0    | 200s     | 7m/s<     | 2000     |
| slow_long_1    | 200s     | 7m/s<     | 2000     |
| slow_curve_0    | 280s     | 7m/s<     | 2800     |
| slow_curve_1    | 150s     | 7m/s<     | 1400     |
| slow_long_curve_0    | 480s     | 7m/s<     | 4800     |
| high_long_0    | 50s     | 7m/s~20ms     | 520     |
| high_long_1    | 70s     | 7m/s~20ms     | 700     |
| high_curve_0    | 260s     | 7m/s~20ms     | 2600     |
| high_long_curve_0    | 260s     | 7m/s~20ms     | 2600     |
| high_long_curve_1    | 230s     | 7m/s~20ms     | 2240     |
| high_long_curve_2    | 300s     | 7m/s~20ms     | 3000     |
| high_long_curve_3    | 280s     | 7m/s~20ms     | 2800     |


## 测试基线 Test baseline
位置信息：/a2rl/observer/ego_loc
速度信息：/a2rl/vn/ins(秒速)或/a2rl/eav24_bsu/kistler_correvit(时速)
航向信息：/a2rl/observer/ego_state

RMSE: Mean Squared Error，均方根误差，评估估计位置与真实位置之间的误差
ATE: Absolute Trajectory Error,绝对轨迹误差，评估估计轨迹与真实轨迹的全局一致性
RPE： Relative Error, 相对位姿误差，评估邻帧之间的相对位姿误差

## 话题类别 Topic classification
velocity

linear velocity:

/a2rl/eav24_bsu/kistler_correvit

/a2rl/eav24_bsu/kistler_vel_angle

/localization/twist_estimator/twist_from_ins

/a2rl/observer/ego_state

/a2rl/vn/ins

/vectornav/raw/ins



angular rate:

/a2rl/eav24_bsu/kistler_vel_angle

/localization/twist_estimator/twist_from_ins

/a2rl/observer/ego_state

/a2rl/vn/ins

/vectornav/raw/ins



wheel velocity:

/a2rl/eav24_bsu/wheels_speed_01



acceleration:

/a2rl/eav24_bsu/kistler_acc_body

/a2rl/eav24_bsu/kistler_angle_vel_body

/a2rl/eav24_bsu/kistler_vel_angle

/a2rl/vn/ins

/vectornav/raw/ins



position:

/a2rl/observer/ego_loc

/vectornav/raw/gps
/vectornav/raw/gps2

/a2rl/vn/ins



imu:

/vectornav/raw/imu



LiDAR:

/sensor/lidar_front/points
/sensor/lidar_left/points
/sensor/lidar_right/points


other:

/vectornav/raw/time

/vectornav/raw/attitude

/a2rl/eav24_bsu/kistler_distance