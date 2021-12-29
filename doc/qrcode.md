# 免费开放api

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

### 生成二维码（图片）
接口地址: `https://open-api.lmikoto.online/api/qrcode/generate/image?content=${content}&size=${size}`   
请求方式: `GET`  

#### 请求参数
|  参数   | 含义  | 是否必填 |
|  ----  | ----  | ---- |
| content  | 二维码内容  | 是 | 
| size  | 二维码大小 默认 300  | 否 |
#### 返回参数
直接返回图片

#### 请求示例
https://open-api.lmikoto.online/api/qrcode/generate/image?content=https://github.com/lmikoto/open-api&size=200
#### 返回结果示例 
<center class="half">
    <img src="/imgs/qr-example.png" width="200"/>
</center>
