# alidayu
阿里大于php-sdk

### 安装
``` bash
composer require sayue/alidayu-sdk
```

### 使用方法
发送短信
``` bash
use Alibaba\taobao\top\TopClient;
use Alibaba\taobao\top\request\AlibabaAliqinFcSmsNumSendRequest;

$c = new TopClient();
$c->appkey = $appkey;
$c->secretKey = $secretKey;

$mobile = 'xxx';    //手机号码
$code = 'xxx'       //短信内容

$req = new AlibabaAliqinFcSmsNumSendRequest();
$req->setSmsType("xxx");
$req->setSmsFreeSignName("xxx");

$req->setSmsParam("{\"code\":\"$code\"}");
$req->setRecNum($mobile);
$req->setSmsTemplateCode("xxx");

$resp = $this->c->execute($req);
return $resp;
```
