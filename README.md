- [cn](#操作指南)
- [en](#Instructions)
# 操作指南

>此SDK仅适用于以下产品型号:
> - LDROBOT LiDAR LD19
## 0. 获取雷达的Linux SDK
```bash
$ cd ~

$ mkdir  ldlidar_ws

$ cd ldlidar_ws

$ git clone  https://github.com/DFRobotdl/ldlidar_stl_sdk.git
```

## 1. 系统设置
- 第一步，通过板载串口或者USB转串口模块(例如,cp2102模块)的方式使雷达连接到你的系统主板.
- 第二步，设置雷达在系统中挂载的串口设备-x权限(以/dev/ttyUSB0为例)
	- 实际使用时，根据雷达在你的系统中的实际挂载情况来设置，可以使用`ls -l /dev`命令查看.

``` bash
$ cd ~/ldlidar_ws/ldlidar_stl_sdk

$ sudo chmod 777 /dev/ttyUSB0
```

## 2. 编译

```bash
$ cd ~/ldlidar_ws/ldlidar_stl_sdk

$ ./auto_build.sh
```

## 3. 运行
  ``` bash
  $ ./build/ldlidar_stl <serial_number>
  # 例如 ./build/ldlidar_stl /dev/ttyS0
  ```

# Instructions
> This SDK is only applicable to the following product models:
> - LDROBOT LiDAR LD19
## 0. get LiDAR Linux SDK
```bash
$ cd ~

$ mkdir  ldlidar_ws

$ cd ldlidar_ws

$ git clone  https://github.com/DFRobotdl/ldlidar_stl_sdk.git
```
## step 1: system setup
- Connect the LiDAR to your system motherboard via an onboard serial port or usB-to-serial module (for example, CP2102 module).

- Set the -x permission for the serial port device mounted by the radar in the system (for example, /dev/ttyUSB0)

  - In actual use, the LiDAR can be set according to the actual mounted status of your system, you can use 'ls -l /dev' command to view.

``` bash
$ cd ~/ldlidar_ws/ldlidar_stl_sdk

$ sudo chmod 777 /dev/ttyUSB0
```

## step 2: build

``` bash
$ cd ~/ldlidar_ws/ldlidar_stl_sdk

$ ./auto_build.sh
```

## step 3: run

  ``` bash
  $ ./build/ldlidar_stl <serial_number>
  # eg ./build/ldlidar_stl /dev/ttyS0
  ```