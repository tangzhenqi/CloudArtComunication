# 获取扮演角色的临时身份凭证完整工程示例

该项目为AssumeRole的完整工程示例。

该示例**无法在线调试**，如需调试可下载到本地后替换 [AK](https://usercenter.console.aliyun.com/#/manage/ak) 以及参数后进行调试。

## 运行条件

- 下载并解压需要语言的代码;


- 在阿里云帐户中获取您的 [凭证](https://usercenter.console.aliyun.com/#/manage/ak) 并通过它替换下载后代码中的 ACCESS_KEY_ID 以及 ACCESS_KEY_SECRET;

- 执行对应语言的构建及运行语句

## 执行步骤

下载的代码包，在根据自己需要更改代码中的参数和 AK 以后，可以在**解压代码所在目录下**按如下的步骤执行：

- *Python 版本要求 Python3*
```sh
python3 setup.py install && python ./alibabacloud_sample/sample.py
```
## 使用的 API

-  AssumeRole：通过调用AssumeRole接口，获取一个扮演RAM角色的临时身份凭证（STS Token）。 更多信息可参考：[文档](https://next.api.aliyun.com/document/Sts/2015-04-01/AssumeRole)

## API 返回示例

*实际输出结构可能稍有不同，属于正常返回；下列输出值仅作为参考，以实际调用为准*


- JSON 格式 
```js
{
  "RequestId": "6894B13B-6D71-4EF5-88FA-F32781734A7F",
  "AssumedRoleUser": {
    "AssumedRoleId": "34458433936495****:alice",
    "Arn": "acs:ram::123456789012****:role/adminrole/alice"
  },
  "Credentials": {
    "SecurityToken": "********",
    "Expiration": "2015-04-09T11:52:19Z",
    "AccessKeySecret": "wyLTSmsyPGP1ohvvw8xYgB29dlGI8KMiH2pK****",
    "AccessKeyId": "STS.L4aBSCSJVMuKg5U1****"
  }
}
```

