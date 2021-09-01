# 概述

本文档为 VisbodyFit-Air 单机版数据接口说明文档。

## 访问地址

本文档所描述的接口全部通过 `http` 访问，访问地址为：`工作站IP和服务端口`，具体地址找运维确认。

## 版本控制

相同接口的不同版本会通过 url 中增加版本号区分，目前版本为`v1`版，访问示例：

> `http://[工作站IP]:[数据接口端口]/v1/[接口地址]`

## 请求参数

每个接口都会说明当前接口的 HTTP 请求方法。
如果是 GET/DELETE 接口，则请求参数通过 query string 传入；
如果是 POST/PUT 接口，则请求参数通过 http body 传入，格式为 JSON。

## 错误处理

所有的接口采用全局统一的错误码，错误响应的状态码 HTTP CODE 为 `400`，响应内容中的具体业务码见 `错误码说明` 。
例如，Token 无效时，接口会返回：

```json
{
  "code": 40003,
  "error_msg": "Invalid Token"
}
```

# 设备对接

## 时序图

# 接口凭证

## 获取接口凭证

获取调用维塑接口的接口凭证

### 请求路径

> `GET /v1/token`

### 参数说明

| 参数名 | 必填 | 类型   | 说明                                             |
| ------ | ---- | ------ | ------------------------------------------------ |
| key    | Yes  | string | 第三方用户唯一凭证，即 vfid,通过维塑管理平台获取 |
| secret | Yes  | string | 第三方用户唯一凭证密钥，即 vfsecret              |

### 响应说明

#### 状态码 200

| 参数名     | 必填 | 类型   | 说明                   |
| ---------- | ---- | ------ | ---------------------- |
| token      | Yes  | string | 接口凭证               |
| expires_in | Yes  | int    | 凭证有效时间，单位秒 s |

#### 示例

```json
{
  "code": 0,
  "data": {
    "token": "TOKEN",
    "expires_in": 7200
  }
}
```

#### 凭证使用方式

接口请求时，将 Token 放入 HTTP Header 中，以获取 TOKEN 信息接口为例，请求如下：

```bash
curl -i http://[工作站IP]:[数据接口端口]/v1/token -H 'Authorization: Bearer <VF-Token>'
```

**注意:** 需要替换请求中的 `<VF-Token>`为实际 Token 值即可

# 体成分测量

## 获取体成分测量文件

获取体成分测量成功后生成的模型、围度 json 文件

### 请求路径

> `GET /v1/measure/file`

### 参数说明

| 参数名  | 必填 | 类型   | 说明     |
| ------- | ---- | ------ | -------- |
| token   | Yes  | string | 接口凭证 |
| scan_id | Yes  | string | 扫描 ID  |

### 响应说明

#### 状态码 200

| 参数名                         | 必填 | 类型   | 说明                         |
| ------------------------------ | ---- | ------ | ---------------------------- |
| model_url                      | Yes  | string | 模型文件路径，文件格式 .obj  |
| json_url                       | Yes  | string | 围度文件路径，文件格式 .json |
| 配合模型文件展示围度位置及数据 |
| expires_in                     | Yes  | int    | 凭证有效时间，单位秒 s       |

#### 示例

```json
{
  "code": 0,
  "data": {
    "model_url": "MODEL_URL",
    "json_url": "JSON_URL",
    "expires_in": 7200
  }
}
```

## 获取体成分测量数据

获取体成分测量成功后得到的体成分数据

### 请求路径

> `GET /v1/measure/data`

### 参数说明

| 参数名  | 必填 | 类型   | 说明     |
| ------- | ---- | ------ | -------- |
| token   | Yes  | string | 接口凭证 |
| scan_id | Yes  | string | 扫描 ID  |

### 响应说明

#### 状态码 200

| 参数名  | 必填 | 类型   | 说明                        |
| ------- | ---- | ------ | --------------------------- |
| WT      | Yes  | object | 体重（kg）                  |
| FFM     | Yes  | object | 去脂体重（kg）              |
| BFM     | Yes  | object | 体脂肪量（kg）              |
| LM      | Yes  | object | 肌肉量（kg）                |
| TBW     | Yes  | object | 身体水分（kg）              |
| BMI     | Yes  | object | 身体质量                    |
| PBF     | Yes  | object | 体脂肪率（%）               |
| BMR     | Yes  | object | 基础代谢量（kcal/d）        |
| WHR     | Yes  | object | 腰臀比                      |
| SM      | Yes  | object | 骨骼肌量（kg）              |
| TM      | Yes  | object | 无机盐（kg）                |
| PROTEIN | Yes  | object | 蛋白质（kg）                |
| l       | Yes  | float  | 测量项下限值                |
| m       | Yes  | float  | 测量项标准值                |
| h       | Yes  | float  | 测量项上限值                |
| v       | Yes  | float  | 测量项测量值                |
| l       | Yes  | int    | 测量项状态 1 低 2 正常 3 高 |

#### 示例

```json
{
  "code": 0,
  "data": {
    "WT": { "l": 10, "m": 15, "h": 20, "v": 30.3, "status": 3 },
    "FFM": { "l": 10, "m": 15, "h": 20, "v": 30.3, "status": 3 },
    "BFM": { "l": 10, "m": 15, "h": 20, "v": 30.3, "status": 3 },
    "LM": { "l": 10, "m": 15, "h": 20, "v": 30.3, "status": 3 },
    "TBW": { "l": 10, "m": 15, "h": 20, "v": 30.3, "status": 3 },
    "BMI": { "l": 10, "m": 15, "h": 20, "v": 30.3, "status": 3 },
    "PBF": { "l": 10, "m": 15, "h": 20, "v": 30.3, "status": 3 },
    "BMR": { "l": 10, "m": 15, "h": 20, "v": 30.3, "status": 3 },
    "WHR": { "l": 10, "m": 15, "h": 20, "v": 30.3, "status": 3 },
    "SM": { "l": 10, "m": 15, "h": 20, "v": 30.3, "status": 3 },
    "TM": { "l": 10, "m": 15, "h": 20, "v": 30.3, "status": 3 },
    "PROTEIN": { "l": 10, "m": 15, "h": 20, "v": 30.3, "status": 3 }
  }
}
```

## 获取围度测量数据

获取体成分测量成功后得到的围度数据

### 请求路径

> `GET /v1/measure/girth`

### 参数说明

| 参数名  | 必填 | 类型   | 说明     |
| ------- | ---- | ------ | -------- |
| token   | Yes  | string | 接口凭证 |
| scan_id | Yes  | string | 扫描 ID  |

### 响应说明

#### 状态码 200

| 参数名                | 必填 | 类型  | 说明           |
| --------------------- | ---- | ----- | -------------- |
| bust_girth            | Yes  | float | 胸围（cm）     |
| waist_girth           | Yes  | float | 腰围（cm）     |
| hip_girth             | Yes  | float | 臀围（cm）     |
| left_upper_arm_girth  | Yes  | float | 左上臂围（cm） |
| right_upper_arm_girth | Yes  | float | 右上臂围（cm） |
| right_thigh_girth     | Yes  | float | 左大腿围（cm） |
| right_thigh_girth     | Yes  | float | 右大腿围（cm） |
| left_calf_girth       | Yes  | float | 左小腿围（cm） |
| right_calf_girth      | Yes  | float | 右小腿围（cm） |
| height                | Yes  | float | 输入身高（cm） |

#### 示例

```json
{
  "code": 0,
  "data": {
    "bust_girth": 30.6,
    "waist_girth": 30.8,
    "hip_girth": 93.8,
    "left_upper_arm_girth": 90,
    "right_upper_arm_girth": 99.8,
    "left_thigh_girth": 58,
    "right_thigh_girth": 56.2,
    "left_calf_girth": 37.1,
    "right_calf_girth": 34.5,
    "height": 161.1
  }
}
```

## 获取用户身体状态

获取体成分测量成功后得到的身体状态及预测年龄

### 请求路径

> `GET /v1/body/state`

### 参数说明

| 参数名  | 必填 | 类型   | 说明     |
| ------- | ---- | ------ | -------- |
| token   | Yes  | string | 接口凭证 |
| scan_id | Yes  | string | 扫描 ID  |

### 响应说明

#### 状态码 200

| 参数名                              | 必填 | 类型 | 说明         |
| ----------------------------------- | ---- | ---- | ------------ |
| body_age                            | Yes  | int  | 预测年龄     |
| body_share                          | Yes  | int  | 体型         |
| 1 虚弱型 2 肌肉型 3 肥胖型 4 健康型 |
| va_grade                            | Yes  | int  | 内脏脂肪等级 |

1~10 正常
10~14 过高
14~17 高

> 17 超高 |

#### 示例

```json
{
  "code": 0,
  "data": {
    "body_age": 18,
    "body_share": 1,
    "va_grade": 9
  }
}
```

#

# 状态码说明

| 代码  | 描述     |
| ----- | -------- |
| -1    | 系统繁忙 |
| 0     | 请求成功 |
| 40001 |          |
| 40002 |          |
| 40003 |          |
|       |          |
|       |          |
|       |          |
