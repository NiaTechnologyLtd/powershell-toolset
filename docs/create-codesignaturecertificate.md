# **Create-CodeSignatureCertificate**

![PowerShell](../assets/powershell.png)

- **概述**

  - 用于创建 PowerShell 脚本自签名证书。

- **参数说明**

  - **-DnsName**
    - 证书适用于的 DNS 名称。
    - 类型
      - String
    - 默认值
      - developer.wangyucai.net
    - 参数别名
      - ***-DN***
    - 是否必选
      - **否**
  - **-ExpireMonth**
    - 证书超时月数。
    - 类型
      - Int32
    - 默认值
      - 36 *(即：3年)*
    - 参数别名
      - **-Expires**
    - 是否必选
      - **否**
    - 约束
      - 最小值：1
  - **-KeySize**
    - 证书密钥长度。
    - 类型
      - ***选项类型***
    - 默认值
      - 4096
    - 参数别名
      - **-Size**
    - 是否必选
      - **否**
    - 选项值
      1. 4096
      2. 2048
      3. 1024
  - **-FriendlyName**
    - 证书友好名称。
    - 类型
      - String
    - 默认值
      - PowerShell Code Signature
    - 参数别名
      - **-FN**
    - 是否必选
      - **否**

- **参考连接**

  - **Microsoft Docs: [New-SelfSignedCertificate](https://docs.microsoft.com/en-us/powershell/module/pkiclient/new-selfsignedcertificate?view=windowsserver2019-ps#syntax)**

- **使用示例**

  ```powershell
  ## PowerShell 使用示例
  ## 作者：Wang Yucai
  ## 时间：2021-4-2 10:57:42
  
  Microsoft PowerShell
  
  PS:> .\Create-CodeSignatureCertificate.ps1 -DN www.baidu.com -Expires 36 -Size 2048 -FN Baidu.com
  
  PS:> .\Create-CodeSignatureCertificate.ps1 -DnsName www.baidu.com -ExpireMonth 36 -KeySize 4096 -FriendlyName Baidu.com
  ```

  