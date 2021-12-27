# 节假日api

## 使用须知
- 这是由本人利用业余时间开发的开放api
- 免费提供给需要的人。
- 如果api有问题可以联系我就行纠正

## 联系方式
- qq: 710801583
- email: lmikoto@outlook.com

## api列表

### 根据日期查询假期信息
接口地址: `https://open-api.lmikoto.online/api/holiday/info/{date}`  

#### 请求参数
`date`: 为查询的日期，非必填，如果不填代表当前日期
|  参数   | 含义  |
|  ----  | ----  |
| date  | 为查询的日期，非必填，如果不填代表当前日期  |
#### 返回参数
|  参数   | 含义  |
|  ----  | ----  |
| status  | 1: 工作日 2: 补班 3: 假期 4: 周末  |
| rest  | 查询的日期距离今天有多少天  |
| name  | 假期名称  |
 
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
#### 示例
https://open-api.lmikoto.online/api/holiday/info/2022-1-1  
https://open-api.lmikoto.online/api/holiday/info  


### 获取最近的一个假期信息
接口地址: `https://open-api.lmikoto.online/api/holiday/next/holiday/info`   

#### 返回参数
|  参数   | 含义  |
|  ----  | ----  |
| status  | 1: 工作日 2: 补班 3: 假期 4: 周末  |
| rest  | 查询的日期距离今天有多少天  |
| name  | 假期名称  |

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
#### 示例
https://open-api.lmikoto.online/api/holiday/next/holiday/info