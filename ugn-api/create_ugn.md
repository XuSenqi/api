# 创建云联网 - CreateUGN

## 简介

创建云联网









## 定义

### 公共参数

| 参数名 | 类型 | 描述信息 | 必填 |
|:---|:---|:---|:---|
| **Action**     | string  | 对应的 API 指令名称，当前 API 为 `CreateUGN`                        | **Yes** |
| **PublicKey**  | string  | 用户公钥，可从 [控制台](https://console.ucloud.cn/uapi/apikey) 获取                                             | **Yes** |
| **Signature**  | string  | 根据公钥及 API 指令生成的用户签名，参见 [签名算法](api/summary/signature.md)  | **Yes** |

### 请求参数

| 参数名 | 类型 | 描述信息 | 必填 |
|:---|:---|:---|:---|
| **ProjectId** | string | 项目ID。不填写为默认项目，子帐号必须填写。 请参考[GetProjectList接口](https://docs.ucloud.cn/api/summary/get_project_list) |**Yes**|
| **Name** | string | 云联网名称，如果没有传入，默认值为“UGN” |No|
| **Remark** | string | 云联网备注，如果没有传入的话，默认为“” |No|
| **Tag** | string | 业务组Id，如果没有传入，默认值为“Default” |No|

### 响应字段

| 字段名 | 类型 | 描述信息 | 必填 |
|:---|:---|:---|:---|
| **RetCode** | int | 返回状态码，为 0 则为成功返回，非 0 为失败 |**Yes**|
| **Action** | string | 操作指令名称 |**Yes**|
| **Message** | string | 返回错误消息，当 `RetCode` 非 0 时提供详细的描述信息 |No|
| **UGNId** | string | 云联网Id |**Yes**|




## 示例

### 请求示例
    
```
https://api.ucloud.cn/?Action=CreateUGN
&ProjectId=iTPxNnOG
&Remark=RIdpGYZc
&BusinessId=mrTmLSYH
&Name=BxDHMRdj
&InstanceId=rcBxXjyl
&InstanceType=RGleoLXh
&InstanceRegion=wEoAagdv
&InstanceProjectId=XqHJFqnF
&InstanceId=VxEbYLtW
&InstanceType=ZVLXzuwk
&InstanceRegion=BfKJBZLL
&InstanceProjectId=uJcoJzFk
```

### 响应示例
    
```json
{
  "Action": "CreateUGNResponse",
  "Message": "success",
  "RetCode": 0,
  "UGNId": "ugn-nqqqKrvb"
}
```





