### 设备上提示体态和肩部测量项目无法使用（拷盘后替换出现）

#### 现象：在开机时，提示设备正在校准中，设备上提示体态和肩部测量项目无法使用，

#### 原因：标定文件与设备原始标定文件不一致，需要替换

#### 正确替换步骤：

- 拷贝原始设备中的标定文件，替换 scanServer，jointFreedomShoulderServer 中的标定文件 camera1_415.yml.camer2.415.yml,camera3.415.yml,transMatF.yml
- 控制服务中的 camera1.415.yml 替换为原始设备中的标定文件
- 设备 SN 号修改确保之前未注册（查看 device_register_info 确定，是否存在和此设备 mac 地址一样的数据）
- 重启设备端所有服务。

#### 问题说明及分析

**深度相机标定文件上传存入数据库的机制（三种情况）**

背景：云端标定文件在设备存储路径/home/visbodyfit/visfitdevice/controlServer/camera1_415.yml  （在控制服务下）

    本地文件在设备存储路径/home/visbodyfit/visfitdevice/scanServer/camera.yml（在扫描服务下）

    云端数据库中有无标定文件的判定，此**设备sn号**是否在depth_camera_adjust表中有标定数据

1、云端数据库标定文件中的 create_date 在本地标定文件之前

2、云端数据库无标定文件，本地标定文件中无 create_date 字段

3、云端数据库无标定文件，本地标定文件有 create_date 字段，且 create_date 能正确解析

**深度相机标定文件从云端覆盖本地机制（三种情况）**

1、云端数据库有标定文件，云端标定文件中的 create_date 在本地标定文件之后

2、云端数据库有标定文件，在云端标定文件中有 create_date 字段

3、云端数据库有标定文件，本地无标定文件，云端标定文件中无 create_date 字段

#### 代码梳理

控制服务（controlServer）

TaskServerConnect,深度相机文件的上传下载

任务服务（TaskServer）

TaskWork 下 RecvHandle 中相关内容涉及深度相机的传入传出
