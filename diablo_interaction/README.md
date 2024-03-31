# DIABLO Interaction 机器人控制交互节点

​	此节点是机器人控制的基础节点，您需要运行 `diablo_ctrl_node` 获取机器人的控制权限。您可以将您的控制指令以自定义msg : `MotionCtrl` 的格式发送到 `/diablo/MotionCmd` 实现控制效果。



## Serial Port Modification 串口修改

​	机器人默认使用 `x3 pi` 的板载 io `/dev/ttyS3` 进行串口通信，如果您需要对其进行修改，请调整至对应的串口号，并重新编译。

```c++
 //file：diablo_ctrl.cpp
 Hal.init("/dev/ttyS3")
```



## Control instructions 控制指令

| 控制ID               | 数值范围   | 备注                 |
| :------------------- | ---------- | -------------------- |
| CMD_GO_FORWARD(0x08) | ±2.0 m/s   | 负数为向后运动       |
| CMD_GO_LEFT(0x04)    | ±2.0 rad/s | 负数为向右运动       |
| CMD_ROLL_RIGHT(0x09) | ±0.2 rad   | 负数为向左运动       |
| CMD_STAND_UP(0x02)   | 0.0        | 机器人站立           |
| CMD_STAND_DOWN(0x12) | 0.0        | 机器人下蹲           |
|                      |            |                      |
| CMD_PITCH_MODE(0x13) | (0.0，1.0) | 位置模式0，速度模式1 |
| CMD_PITCH(0x03)      | ±0.3 pi    | 位置模式0            |
| CMD_PITCH(0x03)      | ±1.8 rad/s | 速度模式1            |
|                      |            |                      |
| CMD_HEIGH_MODE(0x01) | (0.0，1.0) | 位置模式0，速度模式1 |
| CMD_BODY_UP(0x11)    | 0.0~1.0    | 位置模式0            |
| CMD_BODY_UP(0x11)    | ±0.25 m/s  | 速度模式1            |

> 速度模式，机器人将以指令中数值的速度持续运动。
>
> 位置模式，机器人将以指令中数值代表的固定位置运动。


### Translation in english
# DIABLO Interaction Robot Control Node

This node is the foundational node for robot control. You need to run `diablo_ctrl_node` to obtain control permission for the robot. You can send your control commands in the format of the custom message `MotionCtrl` to `/diablo/MotionCmd` to achieve control effects.

## Serial Port Modification

The robot defaults to using the onboard IO `/dev/ttyS3` of the `x3 pi` board for serial communication. If you need to modify it, please adjust to the corresponding serial port number and recompile.

```c++
 //file：diablo_ctrl.cpp
 Hal.init("/dev/ttyS3")
```


## Control Instructions
Control ID	Value Range	Remarks
CMD_GO_FORWARD(0x08)	±2.0 m/s	Negative value is backward motion
CMD_GO_LEFT(0x04)	±2.0 rad/s	Negative value is rightward motion
CMD_ROLL_RIGHT(0x09)	±0.2 rad	Negative value is leftward motion
CMD_STAND_UP(0x02)	0.0	Robot stands
CMD_STAND_DOWN(0x12)	0.0	Robot squats
CMD_PITCH_MODE(0x13)	(0.0, 1.0)	Position mode 0, speed mode 1
CMD_PITCH(0x03)	±0.3 pi	Position mode 0
CMD_PITCH(0x03)	±1.8 rad/s	Speed mode 1
CMD_HEIGH_MODE(0x01)	(0.0, 1.0)	Position mode 0, speed mode 1
CMD_BODY_UP(0x11)	0.0~1.0	Position mode 0
CMD_BODY_UP(0x11)	±0.25 m/s	Speed mode 1

In speed mode, the robot will continuously move at the speed specified in the command.

In position mode, the robot will move to a fixed position represented by the value in the command.