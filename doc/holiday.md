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
`date`为查询的日期，非必填，如果不填代表当前日期

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
        "rest": 9 // 距离当前日期天数
    }
}
```
#### 示例
https://open-api.lmikoto.online/api/holiday/info/2022-1-1  
https://open-api.lmikoto.online/api/holiday/info  


### 获取最近的一个假期信息
接口地址: `https://open-api.lmikoto.online/api/holiday/next/holiday/info`   

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
        "rest": 9 // 距离当前日期天数
    }
}
```
#### 示例
https://open-api.lmikoto.online/api/holiday/next/holiday/info