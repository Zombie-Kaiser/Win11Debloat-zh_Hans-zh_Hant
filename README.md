# Win11Debloat 中文版

[![GitHub Release](https://img.shields.io/github/v/release/Zombie-Kaiser/Win11Debloat-zh_Hans-zh_Hant?style=for-the-badge&label=最新发布)](https://github.com/Zombie-Kaiser/Win11Debloat-zh_Hans-zh_Hant/releases/latest)
[![Join the Discussion](https://img.shields.io/badge/加入-讨论-2D9F2D?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Zombie-Kaiser/Win11Debloat-zh_Hans-zh_Hant/discussions)
[![Static Badge](https://img.shields.io/badge/文档-_?style=for-the-badge&logo=bookstack&color=grey)](https://github.com/Raphire/Win11Debloat/wiki/)

Win11Debloat 是一个轻量级、易于使用的 PowerShell 脚本，可帮助您快速清理和定制 Windows 体验，无需安装！您可以用它来移除预装应用、禁用遥测、去除侵入性界面元素等等。无需费心逐一调整设置或逐个卸载应用，Win11Debloat 让整个过程快速而简单！

本脚本还包含许多系统管理员和高级用户会喜欢的功能，如强大的命令行界面、Windows 审计模式支持，以及对其他 Windows 用户进行更改的能力。您还可以轻松导出和导入您的偏好设置，以便在所有系统上快速应用相同的配置。详情请参阅我们的 [wiki](https://github.com/Raphire/Win11Debloat/wiki)。

本分支基于 [Raphire/Win11Debloat](https://github.com/Raphire/Win11Debloat)，增加了**简体中文 (zh-Hans)** 和**繁体中文 (zh-Hant)** 本地化支持，并提供单文件 EXE 版本。

![Win11Debloat 菜单](/Assets/Images/menu.png)

#### 此脚本对您有帮助吗？请考虑请作者喝杯咖啡以支持他的工作

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/M4M5C6UPC)

## 使用方法

> [!Warning]
> 尽管已尽力确保此脚本不会意外破坏任何系统功能，但使用风险自负！如遇任何问题，请[在此报告](https://github.com/Zombie-Kaiser/Win11Debloat-zh_Hans-zh_Hant/issues)。

### 快速方法（EXE 单文件版）

下载最新发布的 `Win11Debloat.exe` 单文件版本，双击即可运行。无需安装 PowerShell 或任何其他依赖。

1. 从 [GitHub Release](https://github.com/Zombie-Kaiser/Win11Debloat-zh_Hans-zh_Hant/releases/latest) 下载 `Win11Debloat.exe`。
2. 双击运行 `Win11Debloat.exe`。
3. 接受 Windows UAC 提示以管理员身份运行（脚本运行需要管理员权限）。
4. 仔细阅读并按照屏幕上的说明操作。

### 快速方法（PowerShell 一键命令）

通过 PowerShell 自动下载并运行脚本。

1. 打开 PowerShell 或终端。
2. 将以下命令复制粘贴到 PowerShell 中：

```PowerShell
& ([scriptblock]::Create((irm "https://raw.githubusercontent.com/Zombie-Kaiser/Win11Debloat-zh_Hans-zh_Hant/master/Win11Debloat.ps1")))
```

3. 等待脚本自动下载并启动 Win11Debloat。
4. 仔细阅读并按照屏幕上的说明操作。

此方法支持命令行参数以自定义脚本行为。详情请点击[此处](https://github.com/Raphire/Win11Debloat/wiki/Command%E2%80%90line-Interface#parameters)。

### 传统方法

<details>
  <summary>手动下载并运行脚本。</summary><br/>

  1. [下载最新版本的脚本](https://github.com/Zombie-Kaiser/Win11Debloat-zh_Hans-zh_Hant/releases/latest)，并将 .ZIP 文件解压到您选择的位置。
  2. 导航到 Win11Debloat 文件夹。
  3. 双击 `Run.bat` 文件启动脚本。注意：如果控制台窗口立即关闭且没有任何反应，请尝试下面的高级方法。
  4. 接受 Windows UAC 提示以管理员身份运行，这是脚本运行所必需的。
  5. 仔细阅读并按照屏幕上的说明操作。
</details>

### 高级方法

<details>
  <summary>手动下载脚本并通过 PowerShell 运行。推荐高级用户使用。</summary><br/>

  1. [下载最新版本的脚本](https://github.com/Zombie-Kaiser/Win11Debloat-zh_Hans-zh_Hant/releases/latest)，并将 .ZIP 文件解压到您选择的位置。
  2. 以管理员身份打开 PowerShell 或终端。
  3. 临时启用 PowerShell 执行权限，输入以下命令：

  ```PowerShell
  Set-ExecutionPolicy Bypass -Scope Process -Force
  ```

  4. 在 PowerShell 中，导航到文件解压的目录。例如：`cd c:\Win11Debloat`
  5. 输入以下命令运行脚本：

  ```PowerShell
  .\Win11Debloat.ps1
  ```

  6. 仔细阅读并按照屏幕上的说明操作。

  此方法支持命令行参数以自定义脚本行为。详情请点击[此处](https://github.com/Raphire/Win11Debloat/wiki/Command%E2%80%90line-Interface#parameters)。
</details>

### 从源码构建 EXE

<details>
  <summary>使用 ps2exe 从源码构建单文件 EXE。</summary><br/>

  1. 克隆或下载本仓库。
  2. 打开 PowerShell，导航到项目目录。
  3. 运行构建脚本：

  ```PowerShell
  .\Build-Exe.ps1
  ```

  4. 生成的 `Win11Debloat.exe` 将出现在项目根目录中。

  构建脚本会自动安装 `ps2exe` 模块（如未安装），将所有运行时文件打包为 ZIP，嵌入到启动器脚本中，然后编译为单文件 EXE。
</details>

## 功能

以下是 Win11Debloat 提供的主要功能和特性概览。详情请访问 [wiki](https://github.com/Raphire/Win11Debloat/wiki)。

> [!Tip]
> Win11Debloat 所做的所有更改都可以轻松还原，几乎所有应用都可以通过 Microsoft Store 重新安装。关于还原更改的详情请访问 [wiki](https://github.com/Raphire/Win11Debloat/wiki/Reverting-Changes)。

#### 应用移除

- 移除各种预装应用。详情请点击[此处](https://github.com/Raphire/Win11Debloat/wiki/App-Removal)。

#### 隐私与推荐内容

- 禁用遥测、诊断数据、活动历史记录、应用启动跟踪和定向广告。
- 禁用 Windows、锁屏和 Microsoft Edge 中的提示、技巧、建议和广告。
- 禁用 Windows 定位服务、应用定位访问和"查找我的设备"位置跟踪。
- 隐藏设置"主页"页面上的 Microsoft 365 广告，或完全隐藏"主页"页面。

#### AI 功能

- 禁用并移除 Microsoft Copilot、Windows Recall 和 Click to Do。
- 阻止 AI 服务 (WSAIFabricSvc) 自动启动。
- 禁用 Edge、Chrome、Paint 和 Notepad 中的 AI 功能。

#### 系统

- 禁用用于共享和移动文件的拖动托盘。
- 恢复经典 Windows 10 样式右键菜单。
- 关闭"提高指针精确度"（鼠标加速）。
- 禁用粘滞键键盘快捷键。
- 禁用存储感知自动磁盘清理。
- 禁用快速启动以确保完全关机。
- 禁用 BitLocker 自动设备加密。
- 禁用现代待机期间的网络连接以减少电池消耗。

#### Windows 更新

- 阻止 Windows 在更新可用时立即获取。
- 阻止登录时更新后自动重启。
- 禁用与其他 PC 共享已下载的更新（即传递优化）。
- 阻止 Windows 自动安装设备配套应用，如 LG Monitor App、Alienware Command Center 等。

#### 外观

- 启用系统和应用的深色模式。
- 禁用透明效果、动画和视觉效果。
- 隐藏桌面聚光灯的"了解此图片"快捷方式，或完全禁用 Windows 聚光灯背景选项。

#### 开始菜单与搜索

- 自定义开始菜单：移除固定应用、隐藏推荐内容、自定义"所有应用"部分。
- 禁用开始菜单中的手机链接移动设备集成。
- 禁用 Windows 搜索中的 Bing 网络搜索和 Copilot 集成，以及 Microsoft Store 应用建议。

#### 任务栏

- 更改任务栏对齐方式。
- 自定义或隐藏任务栏按钮，如搜索栏、任务视图等。
- 禁用任务栏和锁屏上的小组件。
- 在任务栏右键菜单中启用"结束任务"选项，以快速强制关闭应用。
- 在任务栏应用区域启用"最后活动点击"行为，允许您通过反复点击任务栏上的应用图标在其打开的窗口之间切换焦点。
- 自定义任务栏上应用按钮的显示方式。

#### 文件资源管理器

- 更改文件资源管理器默认打开位置。
- 显示已知文件类型的文件扩展名。
- 显示隐藏的文件、文件夹和驱动器。
- 从文件资源管理器导航窗格隐藏主页、图片库或 OneDrive 部分。
- 隐藏文件资源管理器导航窗格中重复的可移动驱动器条目，只保留"此电脑"下的条目。
- 将所有常用文件夹（桌面、下载等）添加回文件资源管理器中的"此电脑"。
- 更改文件资源管理器中驱动器号的位置或可见性。

#### 多任务处理

- 禁用窗口贴靠。
- 禁用拖动或贴靠窗口时的贴靠助手和贴靠布局建议。
- 更改贴靠窗口或按 Alt+Tab 时是否显示标签页。

#### Windows 可选功能

- 启用 Windows 沙盒，一个用于安全隔离运行应用程序的轻量级桌面环境。
- 启用 Windows Subsystem for Linux，允许您在 Windows 上直接运行 Linux 环境。

#### 其他

- 禁用 Xbox Game Bar 集成和游戏/屏幕录制。这也会在卸载 Xbox Game Bar 后禁用 `ms-gamingoverlay`/`ms-gamebar` 弹窗。
- 禁用 Brave 浏览器中的臃肿功能（AI、加密货币、新闻等）。

#### 高级功能

- 能够[对其他用户应用更改](https://github.com/Raphire/Win11Debloat/wiki/Advanced-Features#running-as-another-user)，而非当前登录用户。
- [Sysprep 模式](https://github.com/Raphire/Win11Debloat/wiki/Advanced-Features#sysprep-mode)，将更改应用到 Windows 默认用户配置文件，确保所有新用户都会自动应用这些更改。

## 语言支持

| 语言 | 代码 | 状态 |
|------|------|------|
| 英语 | en-US | ✅ 完整 |
| 简体中文 | zh-Hans | ✅ 完整 |
| 繁体中文 | zh-Hant | ✅ 完整 |
| 意大利语 | it-IT | ✅ 完整 |
| 荷兰语 | nl-NL | ✅ 完整 |
| 葡萄牙语（巴西） | pt-BR | ✅ 完整 |

## 贡献

欢迎各种形式的贡献！请参阅我们的[贡献指南](https://github.com/Zombie-Kaiser/Win11Debloat-zh_Hans-zh_Hant/blob/master/.github/CONTRIBUTING.md)了解详细说明和最佳实践。

## 许可证

Win11Debloat 基于 MIT 许可证发布。详情请参阅 LICENSE 文件。

---

# Win11Debloat (English)

[![GitHub Release](https://img.shields.io/github/v/release/Zombie-Kaiser/Win11Debloat-zh_Hans-zh_Hant?style=for-the-badge&label=Latest%20release)](https://github.com/Zombie-Kaiser/Win11Debloat-zh_Hans-zh_Hant/releases/latest)
[![Join the Discussion](https://img.shields.io/badge/Join-the%20Discussion-2D9F2D?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Zombie-Kaiser/Win11Debloat-zh_Hans-zh_Hant/discussions)
[![Static Badge](https://img.shields.io/badge/Documentation-_?style=for-the-badge&logo=bookstack&color=grey)](https://github.com/Raphire/Win11Debloat/wiki/)

Win11Debloat is a lightweight, easy to use PowerShell script that allows you to quickly declutter and customize your Windows experience, no installation required! You can use it to remove pre-installed apps, disable telemetry, remove intrusive interface elements and much more. No need to painstakingly go through all the settings yourself or remove apps one by one. Win11Debloat makes the process quick and easy!

The script also includes many features that system administrators and power users will enjoy. Such as a powerful command-line interface, support for Windows Audit mode and the ability to make changes to other Windows users. You can also easily export & import your preferred settings, allowing you to quickly apply the same settings on all your systems. Please refer to our [wiki](https://github.com/Raphire/Win11Debloat/wiki) for more details.

This fork is based on [Raphire/Win11Debloat](https://github.com/Raphire/Win11Debloat) and adds **Simplified Chinese (zh-Hans)** and **Traditional Chinese (zh-Hant)** localization support, along with a single-file EXE build.

![Win11Debloat Menu](/Assets/Images/menu.png)

#### Did this script help you? Please consider buying me a cup of coffee to support my work

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/M4M5C6UPC)

## Usage

> [!Warning]
> Great care went into making sure this script does not unintentionally break any OS functionality, but use at your own risk! If you run into any issues, please report them [here](https://github.com/Zombie-Kaiser/Win11Debloat-zh_Hans-zh_Hant/issues).

### Quick method (Single-file EXE)

Download the latest `Win11Debloat.exe` single-file release and double-click to run. No PowerShell or other dependencies required.

1. Download `Win11Debloat.exe` from [GitHub Release](https://github.com/Zombie-Kaiser/Win11Debloat-zh_Hans-zh_Hant/releases/latest).
2. Double-click `Win11Debloat.exe` to run.
3. Accept the Windows UAC prompt to run as administrator (required for the script to function).
4. Carefully read through and follow the on-screen instructions.

### Quick method (PowerShell one-liner)

Download & run the script automatically via PowerShell.

1. Open PowerShell or Terminal.
2. Copy and paste the command below into PowerShell:

```PowerShell
& ([scriptblock]::Create((irm "https://raw.githubusercontent.com/Zombie-Kaiser/Win11Debloat-zh_Hans-zh_Hant/master/Win11Debloat.ps1")))
```

3. Wait for the script to automatically download and launch Win11Debloat.
4. Carefully read through and follow the on-screen instructions.

This method supports command-line parameters to customize the behaviour of the script. Please click [here](https://github.com/Raphire/Win11Debloat/wiki/Command%E2%80%90line-Interface#parameters) for more information.

### Traditional method

<details>
  <summary>Manually download & run the script.</summary><br/>

  1. [Download the latest version of the script](https://github.com/Zombie-Kaiser/Win11Debloat-zh_Hans-zh_Hant/releases/latest), and extract the .ZIP file to your desired location.
  2. Navigate to the Win11Debloat folder
  3. Double click the `Run.bat` file to start the script. NOTE: If the console window immediately closes and nothing happens, try the advanced method below.
  4. Accept the Windows UAC prompt to run the script as administrator, this is required for the script to function.
  5. Carefully read through and follow the on-screen instructions.
</details>

### Advanced method

<details>
  <summary>Manually download the script & run the script via PowerShell. Recommended for advanced users.</summary><br/>

  1. [Download the latest version of the script](https://github.com/Zombie-Kaiser/Win11Debloat-zh_Hans-zh_Hant/releases/latest), and extract the .ZIP file to your desired location.
  2. Open PowerShell or Terminal as an administrator.
  3. Temporarily enable PowerShell execution by entering the following command:

  ```PowerShell
  Set-ExecutionPolicy Bypass -Scope Process -Force
  ```

  4. In PowerShell, navigate to the directory where the files were extracted. Example: `cd c:\Win11Debloat`
  5. Now run the script by entering the following command:

  ```PowerShell
  .\Win11Debloat.ps1
  ```

  6. Carefully read through and follow the on-screen instructions.

  This method supports command-line parameters to customize the behaviour of the script. Please click [here](https://github.com/Raphire/Win11Debloat/wiki/Command%E2%80%90line-Interface#parameters) for more information.
</details>

### Build EXE from source

<details>
  <summary>Build a single-file EXE from source using ps2exe.</summary><br/>

  1. Clone or download this repository.
  2. Open PowerShell and navigate to the project directory.
  3. Run the build script:

  ```PowerShell
  .\Build-Exe.ps1
  ```

  4. The resulting `Win11Debloat.exe` will appear in the project root directory.

  The build script automatically installs the `ps2exe` module if not present, packages all runtime files into a ZIP, embeds it into a launcher script, and compiles to a single-file EXE.
</details>

## Features

Below is an overview of the key features and functionality offered by Win11Debloat. You can visit [the wiki](https://github.com/Raphire/Win11Debloat/wiki) for more details.

> [!Tip]
> All of the changes made by Win11Debloat can easily be reverted and almost all of the apps can be reinstalled through the Microsoft Store. You can visit [the wiki](https://github.com/Raphire/Win11Debloat/wiki/Reverting-Changes) for more information on reverting changes.

#### App Removal

- Remove a wide variety of preinstalled apps. Click [here](https://github.com/Raphire/Win11Debloat/wiki/App-Removal) for more info.

#### Privacy & Suggested Content

- Disable telemetry, diagnostic data, activity history, app-launch tracking & targeted ads.
- Disable tips, tricks, suggestions & ads across Windows, the lock screen and Microsoft Edge.
- Disable Windows location services, app location access and Find My Device location tracking.
- Hide Microsoft 365 ads on the Settings 'Home' page, or hide the 'Home' page entirely.

#### AI Features

- Disable & remove Microsoft Copilot, Windows Recall and Click to Do.
- Prevent AI service (WSAIFabricSvc) from starting automatically.
- Disable AI Features in Edge, Chrome, Paint and Notepad.

#### System

- Disable the Drag Tray for sharing & moving files.
- Restore the old Windows 10 style context menu.
- Turn off Enhance Pointer Precision (mouse acceleration).
- Disable the Sticky Keys keyboard shortcut.
- Disable Storage Sense automatic disk cleanup.
- Disable fast start-up to ensure a full shutdown.
- Disable BitLocker automatic device encryption.
- Disable network connectivity during Modern Standby to reduce battery drain.

#### Windows Update

- Prevent Windows from getting updates as soon as they're available.
- Prevent automatic restarts after updates while signed in.
- Disable sharing of downloaded updates with other PCs, also known as Delivery Optimization.
- Prevent Windows from auto-installing device companion apps, like LG Monitor App, Alienware Command Center and more.

#### Appearance

- Enable dark mode for system and apps.
- Disable transparency, animations and visual effects.
- Hide the 'Learn about this picture' shortcut for desktop spotlight, or disable the Windows spotlight background option entirely.

#### Start Menu & Search

- Customize the start menu by removing pinned apps, hiding recommendations, and customizing the 'All Apps' section.
- Disable the Phone Link mobile devices integration in the start menu.
- Disable Bing web search & Copilot integration and Microsoft Store app suggestions in Windows search.

#### Taskbar

- Change taskbar alignment.
- Customize or hide taskbar buttons like the search bar, taskview and more.
- Disable widgets on the taskbar & lock screen.
- Enable the 'End Task' option in the taskbar right click menu to quickly force-close apps.
- Enable the 'Last Active Click' behavior in the taskbar app area. This allows you to repeatedly click on an application's icon in the taskbar to switch focus between the open windows of that application.
- Customize how app buttons are shown on the taskbar.

#### File Explorer

- Change the default location that File Explorer opens to.
- Show file extensions for known file types.
- Show hidden files, folders and drives.
- Hide the Home, Gallery or OneDrive section from the File Explorer navigation pane.
- Hide duplicate removable drive entries from the File Explorer navigation pane, so only the entry under 'This PC' remains.
- Add all common folders (Desktop, Downloads, etc.) back to 'This PC' in File Explorer.
- Change drive letter position or visibility in File Explorer.

#### Multi-tasking

- Disable window snapping.
- Disable Snap Assist and Snap Layout suggestions when dragging or snapping windows.
- Change whether tabs are shown when snapping windows or pressing Alt+Tab.

#### Optional Windows Features

- Enable Windows Sandbox, a lightweight desktop environment for safely running applications in isolation.
- Enable Windows Subsystem for Linux which allows you to run a Linux environment directly on Windows.

#### Other

- Disable Xbox Game Bar integration & game/screen recording. This also disables `ms-gamingoverlay`/`ms-gamebar` popups if you uninstall the Xbox Game Bar.
- Disable bloat in Brave browser (AI, Crypto, News, etc.)

#### Advanced Features

- Ability to [apply changes to a different user](https://github.com/Raphire/Win11Debloat/wiki/Advanced-Features#running-as-another-user), instead of the currently logged in user.
- [Sysprep mode](https://github.com/Raphire/Win11Debloat/wiki/Advanced-Features#sysprep-mode) to apply changes to the Windows Default user profile. Which ensures, all new users will have the changes automatically applied to them.

## Language Support

| Language | Code | Status |
|----------|------|--------|
| English | en-US | ✅ Complete |
| Simplified Chinese | zh-Hans | ✅ Complete |
| Traditional Chinese | zh-Hant | ✅ Complete |
| Italian | it-IT | ✅ Complete |
| Dutch | nl-NL | ✅ Complete |
| Portuguese (Brazil) | pt-BR | ✅ Complete |

## Contributing

We welcome contributions of all kinds! Please see our [Contributing Guidelines](https://github.com/Zombie-Kaiser/Win11Debloat-zh_Hans-zh_Hant/blob/master/.github/CONTRIBUTING.md) for detailed instructions on how to get started and best practices for contributing.

## License

Win11Debloat is licensed under the MIT license. See the LICENSE file for more information.
