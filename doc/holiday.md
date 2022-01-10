# 节假日api

## 使用须知
- 这是由本人利用业余时间开发的开放api
- 免费提供给需要的人。
- 如果api有问题可以联系我就行纠正

## 联系方式
- qq: 710801583
- email: lmikoto@outlook.com

## 帮服务器减轻一下负担
如果此服务对你有用，并打算长期使用，你可以赞助个1块不嫌少，2块不嫌多，3块可以买包辣条，10块来者不拒。

<center class="half">
    <img src="/imgs/alipay.png" width="200"/> <img src="/imgs/wepay.png" width="200"/>
</center>

## api列表

### 根据日期查询假期信息
接口地址: `https://open-api.lmikoto.online/api/holiday/info/{date}`   
请求方式: `GET`  

#### 请求参数
|  参数   | 含义  |
|  ----  | ----  |
| date  | 为查询的日期，非必填，如果不填代表当前日期  |
#### 返回参数
|  参数   | 含义  |
|  ----  | ----  |
| status  | 1: 工作日 2: 补班 3: 假期 4: 周末  |
| rest  | 查询的日期距离今天有多少天  |
| name  | 假期名称  |

#### 请求示例
https://open-api.lmikoto.online/api/holiday/info/2022-1-1  
https://open-api.lmikoto.online/api/holiday/info  

#### 返回结果示例 
```json
{
    "code": 0,
    "data": {
        "year": 2022,
        "month": 1,
        "day": 1,
        "week": 6,
        "status": 3,
        "name": "元旦",
        "rest": 9
    }
}
```


### 获取最近的一个假期信息
接口地址: `https://open-api.lmikoto.online/api/holiday/next/holiday/info`   
请求方式: `GET`  

#### 返回参数
|  参数   | 含义  |
|  ----  | ----  |
| status  | 1: 工作日 2: 补班 3: 假期 4: 周末  |
| rest  | 查询的日期距离今天有多少天  |
| name  | 假期名称  |

#### 请求示例
https://open-api.lmikoto.online/api/holiday/next/holiday/info

#### 返回结果示例 
```json
{
    "code": 0,
    "data": {
        "year": 2022,
        "month": 1,
        "day": 1,
        "week": 6,
        "status": 3,
        "name": "元旦",
        "rest": 9
    }
}
```

### 获取最近的一年的假期信息
接口地址: `https://open-api.lmikoto.online/api/holiday/next/year/holiday/info`   
请求方式: `GET`  

#### 返回参数
|  参数   | 含义  |
|  ----  | ----  |
| status  | 1: 工作日 2: 补班 3: 假期 4: 周末  |
| rest  | 查询的日期距离今天有多少天  |
| name  | 假期名称  |

#### 请求示例
https://open-api.lmikoto.online/api/holiday/next/year/holiday/info

#### 返回结果示例 
```json
{
    "code": 0,
    "data": [
        {
            "year": 2022,
            "month": 2,
            "day": 1,
            "week": 2,
            "status": 3,
            "name": "春节",
            "rest": 22
        },
        {
            "year": 2022,
            "month": 4,
            "day": 5,
            "week": 2,
            "status": 3,
            "name": "清明",
            "rest": 85
        },
        {
            "year": 2022,
            "month": 5,
            "day": 1,
            "week": 7,
            "status": 3,
            "name": "劳动节",
            "rest": 111
        },
        {
            "year": 2022,
            "month": 6,
            "day": 3,
            "week": 5,
            "status": 3,
            "name": "端午节",
            "rest": 144
        },
        {
            "year": 2022,
            "month": 9,
            "day": 10,
            "week": 6,
            "status": 3,
            "name": "中秋节",
            "rest": 243
        },
        {
            "year": 2022,
            "month": 10,
            "day": 1,
            "week": 6,
            "status": 3,
            "name": "国庆节",
            "rest": 264
        },
        {
            "year": 2023,
            "month": 1,
            "day": 1,
            "week": 7,
            "status": 4,
            "name": "元旦",
            "rest": 356
        }
    ]
}
```
