# self_driving


# 无人驾驶级别

## Level 1. Driver assistance

提供转向及加速支持，例如，巡航控制。
驾驶员需要充分参与，但可以放弃对自治系统的一些控制。

## Level 2. Partical Automation

自动巡航控制、车道保持，驾驶员需要参与自治系统的任何功能。

## Level 3. Conditional Automation

车辆可以自主驾驶，但驾驶员必须准备在必要时随时接管。

## Level 4. No Human Interference

高度自动化，车辆控制、驾驶体验的所有方向，不期望驾驶员的介入。
此时的车辆可能没有方向盘或任何驾驶员控制装置，但车辆可能被限制在某个区域，称之为“地理围栏”，车辆可以在制定的地理围栏内完全自主的运行。

## Level 5. Full Automation

完全自动化，人类可以驾驶的地方（或任何地方）完全自主运行。


# self-Driving汽车的5个核心部件

## 1. Computer vision 计算机视觉

## 2. Sensor fusion 传感器融合

## 3. Localization 定位

## 4. Path planning 路径规划

## 5. Control 控制

# 高精地图数据

用于定位、地标判断、路线规划

但数据的收集是个问题。。。头部公司有更精准的数据，其他公司可能需要几年的时间收集数据，或直接与头部公司合作比较明智？

# 定位方法

## 1. GNSS RTK

GPS原理，相对于不同参考物的相对位置。
GPS是最广泛的GNSS系统。

分成三个部分：
| satellites 卫星（大约30颗）

| Control Stations 控制站

| Receivers 接收器（至少检测到4颗卫星）

GPS接收器不直接探测你与卫星的距离。
首先测量信号的飞行时间，即信号从卫星传播到你的GPS receiver需要多长时间。（Distance = C * Time）

C（光速）≈ 3 * 10^8 m/s

由于光速很大，所以少量的时间误差或造成巨大的距离误差。为了减小误差，卫星配备了高精度的原子钟，同时使用实时运动定位（RTK）在地面建立基站。
将卫星与基站的误差传递给receiver，修正误差。

## 2. 惯性导航

GPS收到障碍物的影响，而且更新速度慢，大约10HZ（每秒10次），惯性导航可以补充。

惯性导航通过测量加速度判断速度位置

使用惯性测量单元（IMU）作为主要组件（包含三轴加速计传感器和陀螺仪）

* IMU的更新频率高，可达1000HZ，因此IMU可以提供更接近实时的位置信息。
* 陀螺仪的作用是将局部坐标转化为全局坐标。

## 3. LiDAR定位

## 4. 视觉定位

# 感知方法

## 1. 计算机视觉 

Detection -> classification -> tracking ->seqmentation

## 2. 摄像头图像 

例如分成RGB三层

## 3. LiDAR 

激光测距
