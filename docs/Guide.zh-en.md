# Codex 守岸人分享包 v3 使用说明 · User Guide

[中文](#中文说明) | [English](#english-guide)

## 中文说明

适用版本 v3　｜　更新日期 2026 年 10 月 21 日

这份说明用于在另一台电脑安装守岸人启动动画和动态背景。v3 优先修改接收电脑实际使用的 Codex；商店目录受保护时，经用户同意安装独立版，再整合日常启动入口，并保留商店原版。

### 一 开始前准备

1. 接收电脑需要已安装并能正常使用 Codex。每台电脑使用自己的账号；分享包不包含发送者的登录信息、聊天记录或项目文件。

2. 当前适配目标为具有已识别资源结构的 Windows x64 版本。不同版本按结构检测，不能保证所有历史或未来版本都适配；不支持的结构会停止安装。

3. 将 Codex-Shorekeeper-Share-v3.zip 完整解压到一个可写文件夹。不要直接在压缩包内运行脚本，也不要只复制 Install.cmd。

### 二 第一次安装按这个顺序操作

1. 运行 Check.cmd，核对显示的“目标安装位置”和“检测版本”。有多个安装时，选择日常使用的 Codex。

2. 运行 Install.cmd。按提示选择安装；如果询问独立版，输入 y 同意，再填写正式安装位置。具体分支见“安装时的两种情况”。

3. 通过 Codex 的“文件 → 退出”结束原应用。安装器会等待，不会强制终止聊天；默认等待最多 5 分钟。

4. 安装完成后，从桌面或开始菜单的“Codex”入口打开，检查启动动画、动态背景，以及按钮和侧栏文字是否清晰。

### 三 分享包中的常用入口

| 文件 | 用途 |
| --- | --- |
| Check.cmd | 检测目标版本、目录及是否能原位修改。 |
| Install.cmd | 安装或原位更新主题。 |
| Integrate.cmd | 为已安装主题的独立版整合原快捷方式和协议入口。 |
| Restore.cmd | 恢复原入口，并恢复上次安装前的程序文件。 |
| Preview.html | 预览素材；浏览器要求操作时，点击播放。 |

### 四 安装时的两种情况

#### 原安装目录可以写入

安装器准备并校验资源，等待目标 Codex 完全退出，再把主题安装到原程序所在目录。以后继续使用原来的启动入口。回滚备份保存在该安装目录的 .shorekeeper 文件夹。

#### 商店原安装目录受保护

1. 出现“是否安装独立版？[y/N]”时，输入 y 或 yes 继续。输入 n 或直接回车将取消。

2. 选择独立版的正式安装目录。直接回车使用默认建议位置：

%LOCALAPPDATA%\Programs\Codex-Shorekeeper

所选目录必须为空，且位于原安装目录和解压文件夹之外。它将作为日常运行的正式应用目录；不要把它当成临时文件夹删除。

3. 完全退出商店原版。安装器复制的是接收电脑已安装的版本，再适配主题；完成后保留商店原版。

### 五 独立版怎样整合原 Codex

数据：独立版使用应用原生默认数据位置，沿用本机现有的配置环境，不额外建立 CodexShorekeeperProfile。账号、聊天和项目能否直接读取，仍取决于原应用的账户状态、版本和系统访问条件。

入口：安装器把可识别、当前用户可写的原快捷方式改为独立版，并创建桌面和开始菜单的“Codex”入口；同时登记当前用户的 codex: 协议。原入口和协议登记会保留备份。

商店应用库中的受保护入口仍会打开商店原版。任务栏可能缓存旧入口；如果点任务栏仍进入旧版，请取消原固定，从新的 Codex 入口打开独立版后重新固定。Windows 若保留了旧协议关联，需要在默认应用设置中确认。

日常使用时先完全退出原版，再打开独立版。两者使用同一数据位置时，原版仍在运行可能接收启动请求，让你看到原版界面。

### 六 安装成功后检查

• 安装器显示实际程序位置及回滚备份位置，没有“安装未完成”错误。

• 从新的 Codex 入口能进入正常聊天界面，启动动画和背景视频可见。

• 按钮和套餐卡片为深蓝底，左侧项目、对话列表使用浅色文字。

### 七 从 v2 升级到 v3

1. 完整解压 v3，运行 Install.cmd，选择你已经在使用的独立版目录。

2. 退出该独立版，等待原位更新完成。已有独立版可写时，会直接更新；无需再选空目录复制另一套应用。

3. 运行 Integrate.cmd，目标选择更新后的独立版。若缺少来源记录，按提示填写原 Codex 或商店原版的安装目录。这里需要的是程序目录，不是聊天项目文件夹。

4. 原版和独立版均退出后，等待入口整合完成，再从桌面“Codex”打开。已完成的整合会验证原记录，保留最初的入口备份。

### 八 恢复安装前的状态

1. 完全退出需要恢复的 Codex，运行 Restore.cmd。

2. 选择实际安装了主题的目录。若使用独立版，就选择独立版目录，不要选择受保护的商店原版目录。

3. 恢复器先恢复原快捷方式和协议，再恢复上次安装前的程序文件。用户数据和商店原版会保留。

恢复依赖正式安装目录中的 .shorekeeper 备份。如果程序或入口已被其他更新改变，恢复器会停止覆盖并保留备份。不要删除 .shorekeeper，也不要手动把旧主程序或资源文件覆盖到新版本。

### 九 Codex 更新以后

官方更新可能覆盖主题。需要重装主题时，先运行 Check.cmd 检测当前实际使用的版本，通过后再运行 Install.cmd。商店原版的更新不等于独立版自动更新，v3 也不承诺独立版跟随商店同步。

### 十 分享给另一台电脑

发送完整的 v3 ZIP、同名 .sha256 校验文件和本说明即可。接收者在自己的电脑上检测和安装；无需发送你已运行的整套应用目录、账号数据、聊天文件或 .shorekeeper 备份。

本次发布 ZIP 的 SHA256 如下。若重新生成分享包，应以新包附带的校验文件为准。

8c39a6799f79f695cf4f928a1352fb48ad623d9b61672b09e0ad838fc4db785f

### 十一 常见问题

#### 装好后还是默认启动页

先通过“文件 → 退出”结束所有原版和独立版窗口，再从新的桌面 Codex 入口打开。若只有任务栏入口错误，重新固定。仅打开 Preview.html 只是预览，不会安装主题。

#### 安装器一直提示等待退出

关闭窗口可能没有结束后台进程，请使用应用的退出菜单。默认 5 分钟后超时会停止；确认目标应用完全退出，再运行安装器。

#### 提示独立版目录不为空

首次安装请选择一个空目录。若该目录就是已有独立版，请回到目标安装选择，直接选它进行原位更新，不要再走首次复制流程。

#### 提示未知结构或适配失败

当前构建没有通过适配检查。保留错误信息、显示的版本和目标路径，停止覆盖程序文件；不能用别的电脑的主程序文件强行替换。

#### 提示无法访问或文件正被占用

确认目标应用已经退出。安装器会短暂重试共享占用错误，仍失败则停止或回滚。保留错误信息及 .shorekeeper 事务文件，待占用解除后重试。

#### 独立版要求重新登录或聊天没有显示

确认当前 Windows 用户、Codex 账号及实际打开的程序位置。v3 沿用应用默认数据逻辑，不承诺在不同版本、账号或系统环境之间自动迁移。不要删除原数据，也不要复制其他人的账号文件。

#### 入口整合提示已有记录或入口被更改

若提示现有入口与备份不一致，请保留 .shorekeeper 和错误信息，不要删除记录强行重装。Restore.cmd 也可能因外部更新而停止，需要先核对备份和当前入口。

### 十二 需要保留的资料

反馈问题时记录安装器错误原文、检测版本、显示的目标安装路径，以及你从哪个入口打开应用。这些信息能区分原版入口、独立版入口与版本适配问题。无需发送登录凭据或聊天内容。

这是本地主题定制包。程序文件经修改后不再具有原厂文件的有效签名，官方更新可能影响定制效果。素材来自提供的视频，分享包不授予原视频或游戏角色的版权。

## English guide

Version v3 · Updated October 21, 2026

This guide explains how to install the Shorekeeper startup animation and video background on another computer. The installer first targets the recipient's actual Codex installation. If its Store directory is protected, it asks whether to install a standalone copy and where to put it, then integrates writable launch entries while retaining the Store version.

### 1 Before you start

1. Codex must already be installed and working on the recipient computer. Each computer uses its own account. The package does not include the sender's login, chats, or project files.
2. The adapter targets recognized Windows x64 resource structures. It does not support every historical or future version; unknown structures stop installation.
3. Fully extract `Codex-Shorekeeper-Share-v3.zip` to a writable folder. Do not run the installer inside the ZIP or copy only `Install.cmd`.

### 2 First installation

1. Run `Check.cmd` and verify the target installation path and detected version. If several installations are listed, choose the one you normally use.
2. Run `Install.cmd`. If asked about a standalone installation, enter `y` to agree and choose a permanent installation directory.
3. Fully quit the original Codex using its exit menu. The installer waits for you and does not forcibly terminate the conversation. The default timeout is five minutes.
4. After installation finishes, launch `Codex` from the desktop or Start menu. Check the startup animation, video background, and text contrast.

### 3 Files you will use

| File | Purpose |
| --- | --- |
| `Check.cmd` | Detect the target version and path, and whether it can be modified in place. |
| `Install.cmd` | Install or update the theme in place. |
| `Integrate.cmd` | Integrate original launch entries with an already themed standalone installation. |
| `Restore.cmd` | Restore original launch entries and the program files from before the most recent install. |
| `Preview.html` | Preview the media; click Play if the browser requires interaction. |

### 4 Installation options

**Writable installation directory:** The installer prepares and verifies resources, waits for Codex to exit, and installs the theme into the original program directory. Keep using the existing launch entries. Recovery backups are stored under `.shorekeeper` in that directory.

**Protected Store directory:**

1. At `是否安装独立版？[y/N]`, enter `y` or `yes` to continue. Enter `n`, or press Enter without typing, to cancel.
2. Choose an empty permanent directory outside both the original installation and the extracted theme package. Press Enter to accept the suggested path:

```text
%LOCALAPPDATA%\Programs\Codex-Shorekeeper
```

3. Fully quit the Store version. The installer copies the version already installed on the recipient computer and adapts the theme. It retains the original Store installation.

The selected standalone directory is your permanent application directory. Do not delete it as if it were a temporary extraction folder.

### 5 How standalone integration works

**Data:** The standalone app uses the application's native default profile logic and the existing local configuration environment. It does not create a separate `CodexShorekeeperProfile`. Whether an existing account, chats, and projects can be read depends on account state, version, and system access conditions.

**Launch entries:** Recognized shortcuts writable by the current user are changed to point to the standalone app. Desktop and Start menu entries named `Codex` are created, and the current user's `codex:` protocol is registered. Original entries and protocol registration are backed up.

Protected entries in the Store library still launch the Store version. Windows may cache old taskbar pins: unpin the old entry, open the standalone app through the new Codex shortcut, then pin it again. If Windows retains the old default protocol choice, confirm the association in Default apps.

Fully quit the original before launching the standalone app. When they use the same profile, an already-running original instance may receive the launch request and display the original interface.

### 6 Confirm installation succeeded

- The installer displays the actual executable and backup paths without an installation failure message.
- The new Codex entry opens the normal chat interface, startup animation, and video background.
- Buttons and plan or usage cards have dark navy backgrounds; project and conversation names in the sidebar use light text.

### 7 Upgrade an existing v2 installation

1. Fully extract v3, run `Install.cmd`, and choose the standalone installation you already use.
2. Quit that installation and wait for the in-place update. An existing writable standalone copy does not need another empty-directory installation.
3. Run `Integrate.cmd` and select the updated standalone copy. If no origin record exists, provide the original Codex or Store application directory. This is the program directory, not a project folder.
4. Let both the original and standalone apps exit while integration finishes. Then open the desktop Codex entry. Repeated integration verifies the existing record and retains the original entry backups.

### 8 Restore the previous state

1. Fully quit the target Codex and run `Restore.cmd`.
2. Select the directory where the theme was installed. For a standalone installation, select its directory rather than the protected Store directory.
3. The restore process restores shortcuts and protocol registration first, followed by the program files from before the most recent install. User data and the Store original are retained.

Recovery requires the `.shorekeeper` backups. If another update has changed the program or launch entries, restoration stops instead of overwriting them and preserves the backups. Do not delete `.shorekeeper` or manually replace newer program files with old copies.

### 9 After Codex updates

Official updates may overwrite the theme. Run `Check.cmd` against the version you actually use, and only reinstall with `Install.cmd` if its structure passes. Updating the Store version does not mean the standalone copy has been updated; v3 does not guarantee automatic synchronization.

### 10 Share with another computer

Send the complete v3 ZIP, its `.sha256` file, and this guide. Recipients detect and install against their own local Codex. Do not share your personal application runtime, account data, chats, or `.shorekeeper` backups.

The SHA256 of this v3 ZIP is:

```text
8c39a6799f79f695cf4f928a1352fb48ad623d9b61672b09e0ad838fc4db785f
```

For a rebuilt package, use the checksum supplied with that new package.

### 11 Troubleshooting

**The default startup page still appears:** Fully quit the original and standalone apps, then use the new desktop Codex entry. Repin the taskbar entry if that is the only entry opening the old app. `Preview.html` only previews media and does not install the theme.

**The installer keeps waiting for exit:** Closing a window may leave the app running. Use its exit menu. The installer stops after the default five-minute timeout; retry once the target has fully exited.

**The standalone destination is not empty:** Choose an empty directory for the first installation. To update an existing standalone copy, select it as the target for an in-place update instead of repeating the initial copy flow.

**Unknown structure or adaptation failure:** The build has not passed the adapter checks. Keep the error, detected version, and path. Do not force the installation by copying another computer's executable.

**Access denied or a file is in use:** Confirm the target app has exited. The installer briefly retries sharing violations, then stops or rolls back if they persist. Keep the error and `.shorekeeper` transaction files and retry after the lock is released.

**The standalone app asks for login or chats are missing:** Check the Windows user, Codex account, and executable path. v3 retains native default profile logic; it does not guarantee migration between different accounts, builds, or system environments. Keep the original data and never copy someone else's account files.

**Integration reports an existing record or changed entries:** Keep `.shorekeeper` and the error. Do not delete the record to force integration. `Restore.cmd` can also stop after external updates; inspect the current entries and backups before proceeding.

### 12 Information to keep when reporting an issue

Keep the exact installer error, detected Codex version, target installation path, and the launch entry you used. These distinguish original-versus-standalone launch issues from compatibility issues. Login credentials and chat contents are not needed.

This is a local theme customization package. Modified executables no longer retain a valid original-vendor signature, and official updates can affect the customization. Original video and game character rights remain with their respective owners; this package does not grant rights to those media.

