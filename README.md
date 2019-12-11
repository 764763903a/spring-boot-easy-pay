### Easy-Pay

<img src="https://github.com/easy-pay/easy-pay/blob/master/doc/logo.jpg" width="700" height="150" alt="logo"/>

![演示gif](https://github.com/easy-pay/spring-boot-easy-pay-demo/blob/master/src/main/resources/demo.png)


#### 使用前配置文件配置如下

- 在项目`pom.xml`文件中引入`Easy-Pay`的依赖，该依赖已经发布到了maven的中央仓库。

```xml
<dependency>
    <groupId>cn.isuyu.boot</groupId>
    <artifactId>easy-pay-spring-boot-starter</artifactId>
    <version>1.0.0</version>
</dependency>
```
#### 配置文件

```yaml
easy:
  pay:
    #支付宝支付参数配置
    alipay:
      #应用ID,您的APPID，收款账号既是您的APPID对应支付宝账号
      appId:
      #商户私钥，您的PKCS8格式RSA2私钥
      privateKey:
      publicKey:
      #服务器异步通知页面路径  需http://格式的完整路径，不能加?id=123这类自定义参数，必须外网可以正常访问
      notifyUrl: http://0b228e36.ngrok.io/alipay/callback
      #页面跳转同步通知页面路径 需http://格式的完整路径，不能加?id=123这类自定义参数，必须外网可以正常访问
      returnUrl: http://0b228e36.ngrok.io/
    #微信支付参数配置
    wxpay:
      #公众号appid
      appId:
      #商户id
      mchId:
      #支付api安全密钥
      mchKey:
      #支付结果回调地址
      payNotify: http://0b228e36.ngrok.io/wx/callback
      #退款结果回调(该值暂时还未使用到，因为退款我并没有做回调，待以后完善吧)
      refundNotify:
      #项目根目录根目录下的证书名称(退款需要用到证书)
      certName: wx_pay_cert.p12

```
- [SpringBoot使用Easy-Pay Demo](https://github.com/easy-pay/spring-boot-easy-pay/tree/master/easy-pay-spring-boot-sample)

- [支付宝支付使用文档](https://github.com/easy-pay/spring-boot-easy-pay/tree/master/docs/alipay.md)

- [微信支付使用文档](https://github.com/easy-pay/spring-boot-easy-pay/tree/master/docs/wxpay.md)

 有问题可以`微信`我

<img width="200" height="200" src="https://github.com/easy-pay/spring-boot-easy-pay/blob/master/docs/wx.png"/>