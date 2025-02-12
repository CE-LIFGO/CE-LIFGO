## intro

《》文章开源仓库

## 硬件
### 物理结构


### 设备

| 名称     | 型号/说明 |
| ----------- | ----------- |
| STM32H750VBT6      | Text       |
| 蓝牙模块   | Text        |
| 光敏二极管   | Text        |
| 激光器   | Text        |


## 代码结构

- `Core`
  - 核心代码。Inc：头文件。Src：各种函数的源文件以及主程序`main.c`。Startup中的.s文件初始化了整个硬件系统（读得懂汇编语言可以看看，里面包含了整个MCU的初始化过程，主程序的入口等）。

- `MDK-ARM`
  - `.uvprojx`为keil工程，用keil打开后已经完成了链接库、编译设置，可以直接编译烧录
  - 链接目录为上一层的`USB_DEVICE`、`Drivers`、`Middlewares`

- 其他
  - `Debug`：编译和链接过程中生成的各种文件和目录
  - `Drivers-CMSIS`：Cortex-M内核相关文件，提供STM32芯片内核和外设访问接口。包含启动文件(`startup_xxx.s`)，负责初始化硬件；以及提供优化库。
  - `Middlewares`、`USB_DEVICE`：库文件，stm32USB驱动
  




## 如何烧录

### 使用STM32CubeIDE烧录


### 使用Keil烧录




















