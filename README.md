# APISpace 介绍
**本 API 服务由 [APISpace（apispace.com）](https://www.apispace.com/?utm_source=github&utm_term=qiyegongshangsiyaosu) 提供。**

APISpace 是 Eolink 旗下专业的 API 开放与交易平台，为广大企业以及个人开发者提供多维度、全方位的API接口，覆盖短信验证、天气查询、快递物流、OCR文字识别等海量 API 服务，帮助用户快速获取数据，降低获取数据的成本和难度，提升开发效率。

APISpace 提供15种开发语言的代码示例，分别是：
- Java(OK HTTP)
- HTTP
- cURL
- 微信小程序
- PHP(pecl_http)、PHP(cURL)
- Python(http.client)、Python(Requests)
- JavaScript(Jquery AJAX)、JavaScript(XHR)
- NodeJS(Native)、NodeJS(Request)
- Ruby(Net:Http)
- Shell(Httpie)、Shell(cUrl)

# 企业工商四要素
传入企业名称、社会统一信用代码、法人名称、法人身份证，校验此四项是否一致。官方权威核验，实时更新。

**使用该产品前，您需要通过 [https://www.apispace.com/eolink/api/gsxx/introduction](https://www.apispace.com/eolink/api/gsxx/introduction?utm_source=github&utm_term=qiyegongshangsiyaosu) 申请API服务**

本文档末尾提供了 Python(Requests) 的调用代码示例，可以前往文档末尾查看。

更多代码示例：[https://www.apispace.com/eolink/api/gsxx/guidence/](https://www.apispace.com/eolink/api/gsxx/guidence/?utm_source=github&utm_term=qiyegongshangsiyaosu)

### 应用场景

1.  #### B2B 电商平台入驻核验

部分针对企业用户的平台，尤其是TO B的平台和政务类平台，每天需要面对数量众多的企业申请，当企业提交自身营业执照信息后，平台就需要快速精准的对申请的企业做出验证，在避免部分风险的同时，获得进一步的商机。


2.  #### 供应链金融平台入驻企业身份核验

当确定与对方进行商务合作前，也需要对对方企业信息进行基础性核验，防范空壳公司僵尸公司的诈骗，提升企业风险防御能力。


3.  #### 商业银行、互联网金融平台贷前法人核验

在市场竞争及市场合作中，企业间需要相互了解。 签订合同、参加投标、申请资格、平台入驻等，为了防止遇到虚假企业、空客公司，规避商务合作中的风险。

### 产品优势
![image](https://user-images.githubusercontent.com/36323798/223959015-e0bfd743-ed81-47fe-89a8-b1e8d21c0984.png)

### Python(Requests) 调用代码示例

```
import requests

url = "https://eolink.o.apispace.com/gsxx/business-four-auth"

payload = {"entName":"","legalPerName":"","creditCode":"","idNum":""}

headers = {
    "X-APISpace-Token":"",
    "Authorization-Type":"apikey",
    "Content-Type":"application/x-www-form-urlencoded"
}

response=requests.request("POST", url, data=payload, headers=headers)

print(response.text)

```
