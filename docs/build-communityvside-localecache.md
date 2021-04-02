# **Build-CommunityVSIDE-LocaleCache**

![PowerShell](../assets/powershell.png)

- **概述**

  - 用于构建 Visual Studio 2019 社区版本地安全包。

- **参数说明**

  - **-VSBootstrapProgramPath**
    - Visual Studio 2019 社区版本地安装包引导程序（[vs_community.exe](https://visualstudio.microsoft.com/thank-you-downloading-visual-studio/?sku=community&rel=16&utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=offline+install&utm_content=download+vs2019)）路径。您也可以使用脚本 [Download-CommunityVSIDE.ps1](./download-communityvside.md) 进行下载。
    - 变量别名
      - **-Setup**
    - 类型
      - String
    - 是否必需
      - **是**
  - **-LocalPath**
    - 安装包本地存储路径。
    - 变量别名
      - **-Save**
    - 类型
      - String
    - 是否必需
      - **是**
  - **-Language**
    - Visual Studio 语言选项。
    - 变量别名
      - **-Lang**
    - 类型
      - ***下拉选项***
    - 默认值
      - zh-CN：**简体中文**
    - 选项
      - zh-CN：简体中文
      - en-US：英语（美国）
  - **-IncludeAzureWorkload (Swith)**
    - 是否包含 **[Microsoft Azure](https://docs.microsoft.com/en-us/visualstudio/install/workload-component-id-vs-community?view=vs-2019&preserve-view=true#azure-development)** 开发工作负载。
  - **-IncludeDataWorkload (Swith)**
    - 是否包含**[数据存储、处理](https://docs.microsoft.com/en-us/visualstudio/install/workload-component-id-vs-community?view=vs-2019&preserve-view=true#data-storage-and-processing)**工作负载。
  - **-IncludeDataAnalysisWorkload (Swith)**
    - 是否包含**[数据科学、分析](https://docs.microsoft.com/en-us/visualstudio/install/workload-component-id-vs-community?view=vs-2019&preserve-view=true#data-science-and-analytical-applications)**工作负载。
  - **-ExcludeDesktopWorkload (Swith)**
    - 是否**排除** **[.NET 桌面开发](https://docs.microsoft.com/en-us/visualstudio/install/workload-component-id-vs-community?view=vs-2019&preserve-view=true#net-desktop-development)**工作负载。
  - **-IncludeUnity3dWorkload (Swith)**
    - 是否包含 **[Unity 3D 游戏开发](https://docs.microsoft.com/en-us/visualstudio/install/workload-component-id-vs-community?view=vs-2019&preserve-view=true#game-development-with-unity)** 工作负载。
  - **-IncludeMobileWorkload**
    - 是否包含**[.NET 跨平台开发](https://docs.microsoft.com/en-us/visualstudio/install/workload-component-id-vs-community?view=vs-2019&preserve-view=true#mobile-development-with-net)**工作负载。
  - **-IncludeNodejsWorkload**
    - 是否包含**[Node.js 开发](https://docs.microsoft.com/en-us/visualstudio/install/workload-component-id-vs-community?view=vs-2019&preserve-view=true#nodejs-development)**工作负载。
  - **-IncludeOfficeWorkload**
    - 是否包含 **[Microsoft Office 开发](https://docs.microsoft.com/en-us/visualstudio/install/workload-component-id-vs-community?view=vs-2019&preserve-view=true#officesharepoint-development)** 工作负载。
  - **-IncludePythonWorkload**
    - 是否包含 **[Python 开发](https://docs.microsoft.com/en-us/visualstudio/install/workload-component-id-vs-community?view=vs-2019&preserve-view=true#python-development)** 工作负载。
  - **-IncludeUwpWorkload**
    - 是否包含 **[Universal Windows Platform (UWP) 开发](https://docs.microsoft.com/en-us/visualstudio/install/workload-component-id-vs-community?view=vs-2019&preserve-view=true#universal-windows-platform-development)** 工作负载。
  - **-IncludeVSExtensionsWorkload**
    - 是否包含 **[Visual Studio 扩展开发](https://docs.microsoft.com/en-us/visualstudio/install/workload-component-id-vs-community?view=vs-2019&preserve-view=true#visual-studio-extension-development)** 工作负载。
  - **-IncludeGithub**
    - 是否包含 **Github** 组件。
  - **-IncludeClickOnce**
    - 是否包含 **ClickOnce** 组件。
  - **-IncludeOldFrameworks**
    - 是否包含旧版本的 **.NET Framework 4.6 ~ 4.7.2** 和 **.NET Core 2.0 & .NET Core 3.0** 组件。
  - **-IncludeClassDesigner**
    - 是否包含 **ClassDesigner** 组件。
  - **-IncludeServiceReference**
    - 是否包含 **[Microsoft.VisualStudio.Component.VisualStudioData](https://docs.microsoft.com/en-us/visualstudio/install/workload-component-id-vs-community?view=vs-2019&preserve-view=true#unaffiliated-components)** 组件。
  - **-IncludeAspNetMvc4**
    - 是否包含 **ASP.NET MVC 4.0** 开发组件。

- **使用示例**

  ```powershell
  ## 用于构建 Visual Studio 2019 社区版本地安装包。
  ## 作者：Wang Yucai
  ## 时间：2021-4-2 14:20:14
  
  PS > .\Build-CommunityVSIDE-LocaleCache.ps1 -Setup "C:\vs_community.exe" -Save "D:\VS2019" -Lang zh-CN -IncludeAspNetMvc4
  ```

  

