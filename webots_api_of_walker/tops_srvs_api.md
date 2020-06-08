## Api for node of "webots"

### 1.Publisher
#### (1) camera_imu, orientus_imu, head_imu
> Walker 配备三个 IMU,分别位于腰部、双目相机与头部,具体分布参考 2.5 小节。目前,
> IMU 反馈角度、角速度及线加速度等信息,角度信息采用欧拉角表示:滚动角(roll)、俯仰角
> (pitch)及偏航角(yaw)。
> 具体反馈信息如下:
> 名称:/sensor/orientus_imu(腰部 IMU)
>     /sensor/camera_imu(双目相机 IMU)
>     /sensor/head_imu(头部 IMU)
> 类型:sensor_msgs/Imu
> 发布频率:1000Hz
> Imu格式 IMU[https://github.com/Dongbox/walker_wiki/blob/master/msg_format.md#1imu]
##### Information
```
topic = "/sensor/camera_imu"
msg_type = Imu
```

##### Usage
```
from utils.walker_tops_srvs import WalkerWebotsPub, build_subscriber

def callback_func(msg):
    ...

camera_imu = WalkerWebotsPub.camera_imu

sub = build_subscriber(camera_imu, callback_func)
```
