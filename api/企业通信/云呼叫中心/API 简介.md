欢迎使用云呼叫中心（Cloud Call Center，CCC）。


云呼叫中心（Cloud Call Center，CCC）为您提供便捷的互动式呼叫中心管理服务。

只需对接 API 接口，您就可以在云端到传统的呼叫中心能力，来实现您的呼叫管理需求。随着业务需求的变化，您可以实时扩展或缩减呼叫管理资源。

云呼叫中心支持按需计费，降低您的系统建设门槛。使用云呼叫中心可以极大降低您的软硬件采购成本，简化客服/营销系统开发工作。

 在使用这些接口前，请确保已按照 [快速入门](https://cloud.tencent.com/document/product/679/14495) 开通了云呼叫中心服务。

## 名词解释
### 呼叫
#### 呼叫类型1：
1、预测式外呼:先接通客户，再接通坐席。
2、预览式外呼:先接通坐席，再接通客户。

### 接口说明
#### 名词约束：

**Callid：**
每次发起的会话 ID 全局唯一，格式为：yyyymmddHHMMSSnnnnnn
最后六位为随机数，如果是呼出类型，会在最后加 “-out”。

**Appid：**
机构 ID，每次请求必须要带上。

#### 通用设定：
在未特别说明的情况下，均遵从以下约定:

**接口**：所有接口均要求使用POST请求；
**事件通知**：（以下标题中包含通知的字段）
**请求方式**：POST
**HTTP 头部**:
```
Accept：application/json
Content-Type：text/json;charset=utf-8
```

要求用户返回结果json字符串：
```
{
		"code": "0",
		"msg": "0"
}

```

#### 接口调用时序:
呼入：
![](https://main.qcloudimg.com/raw/e13cdc449801134c181c49893f55d1b7.png)

呼出：
![](https://main.qcloudimg.com/raw/af1a02914ba97aeec28233047bd0bd5a.png)
