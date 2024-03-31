# Diablo ception 机器人感知模块

​	此模块主要定义了一些用于对机器人感知方面的功能节点。您可以在 `diablo_body` 的实现中调整传感器数据更新或发布的频率。
This module mainly defines some functional nodes for robot perception. You can adjust how often sensor data is updated or published in your implementation of `diablo_body`.


> 并不建议您对其进行调整，过高的频率可能会导致串口数据的错误。
It is not recommended that you adjust it. Too high a frequency may cause serial port data errors.


.

> diablo_battery.hpp ---------------------------->机器人电量信息发布Robot battery information release
>
> diablo_body_state.hpp--------------- -------->机器人运动状态信息发布Robot motion status information release
>
> diablo_imu.hpp---------------------------------->机器人IMU信息发布Robot IMU information release
>
>  diablo_legmotors.hpp------------------------->机器人电机信息发布Robot motor information release

