# DIABLO common function 机器人SDK通用函数

​	这个模块主要实现了对通信协议的处理。用于数据的打包以及解包，用户可以不做了解。
This module mainly implements the processing of communication protocols. Used for data packaging and unpacking, users do not need to understand it.

> diablo_utils
>
> > diablo_tools
> >
> > > onboard_sdk_uart_protocol.h -------------->通信协议结构体定义Communication protocol structure definition
> > >
> > > osdk_crc.hpp-------------------------------------->数据crc校验Data crc verification
> > >
> > > osdk_ddj_m15.hpp------------------------------>m15 电机控制协议m15 motor control protocol
> > >
> > > osdk_hal.hpp-------------------------------------->串口读写操作实现Implementation of serial port read and write operations
> > >
> > > osdk_header.hpp-------------------------------->通信协议包头定义及处理Communication protocol header definition and processing
> > >
> > > osdk_movement.hpp--------------------------->机器人控制方法实现Robot control method implementation
> > >
> > > osdk_telemetry.hpp----------------------------->串口数据解包实现Serial port data unpacking implementation
> > >
> > > osdk_vehicle.hpp--------------------------------->整合调用接口Integrated calling interface
> > >
> > > osdk_virtual_rc.hpp------------------------------>模拟遥控器发送数据Simulate remote control to send data
> >
> > VulcanSerial
> > 
> > > Exception.hpp--------------------------------------->串口异常响应Serial port exception response
> > >
> > > SerialPort.hpp--------------------------------------->对串口库的实现For serial port library accomplish


