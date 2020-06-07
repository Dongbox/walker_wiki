## Api for node of "webots"

### 1.Publisher
#### (1) camera_imu
> introduce
> is here

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
