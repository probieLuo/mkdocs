# ASP.NET Core 入门指南

ASP.NET Core 是微软推出的跨平台、高性能、开源的现代 Web 框架，适用于构建 Web 应用、API 和微服务。本文将带你快速入门 ASP.NET Core 开发。

---

## 1. 环境准备

- **.NET SDK**：前往 [.NET 官网](https://dotnet.microsoft.com/download) 下载并安装最新的 .NET SDK。
- **开发工具**：推荐使用 [Visual Studio](https://visualstudio.microsoft.com/)、[Visual Studio Code](https://code.visualstudio.com/) 或 Rider。

---

## 2. 创建第一个 ASP.NET Core 项目

打开终端或命令提示符，输入以下命令：

```bash
dotnet new webapp -n MyFirstAspNetCoreApp
cd MyFirstAspNetCoreApp
```

- `webapp` 模板用于创建带有 Razor Pages 的 Web 应用。
- `-n` 指定项目名称。

---

## 3. 运行项目

在项目目录下运行：

```bash
dotnet run
```

终端会显示类似如下信息：

```
Now listening on: https://localhost:5001
Now listening on: http://localhost:5000
```

在浏览器访问 [https://localhost:5001](https://localhost:5001) 即可看到默认页面。

---

## 4. 项目结构简介

```
MyFirstAspNetCoreApp/
│
├── Pages/           # Razor Pages 页面
├── wwwroot/         # 静态文件（CSS、JS、图片等）
├── appsettings.json # 配置文件
├── Program.cs       # 应用入口
└── Startup.cs       # 启动配置（.NET 6 及以上合并到 Program.cs）
```

---

## 5. 添加一个新页面

在 `Pages` 文件夹下新建 `Hello.cshtml` 和 `Hello.cshtml.cs`：

**Hello.cshtml**
```html
@page
@model HelloModel
<h2>Hello, ASP.NET Core!</h2>
<p>欢迎来到你的第一个 ASP.NET Core 页面。</p>
```

**Hello.cshtml.cs**
```csharp
using Microsoft.AspNetCore.Mvc.RazorPages;

public class HelloModel : PageModel
{
    public void OnGet()
    {
    }
}
```

---

## 6. 路由访问

在浏览器访问 [https://localhost:5001/Hello](https://localhost:5001/Hello) 即可看到新页面。

---

## 7. 常用命令

- 创建 Web API 项目：  
  ```bash
  dotnet new webapi -n MyApi
  ```
- 添加依赖包：  
  ```bash
  dotnet add package 包名
  ```
- 发布项目：  
  ```bash
  dotnet publish -c Release
  ```

---

## 8. 参考资料

- [ASP.NET Core 官方文档](https://learn.microsoft.com/aspnet/core)
- [Razor Pages 指南](https://learn.microsoft.com/aspnet/core/razor-pages/)

---

祝你玩转 ASP.NET Core！