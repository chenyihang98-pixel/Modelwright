<h3 align="center">
  简体中文 &nbsp;|&nbsp; <a href="README.en.md">English</a> &nbsp;|&nbsp; <a href="README.ja.md">日本語</a>
</h3>

<p align="center">
  <img src="docs/screenshots/02-home.png" alt="模匠首页" width="880">
</p>

<h1 align="center">模匠 Modelwright</h1>

<p align="center"><b>一张图或一句话生成 3D 模型，一键送进 Unity。</b></p>

<p align="center">
  <a href="https://github.com/chenyihang98-pixel/Modelwright/releases/latest">下载</a> ·
  <a href="https://www.bilibili.com/video/BV1YqpZ6kEw4">演示视频</a> ·
  <a href="RELEASE-NOTES.md">更新日志</a> ·
  <a href="https://chenyihang98-pixel.github.io/Modelwright/">介绍页</a>
</p>

<p align="center">
  <a href="https://github.com/chenyihang98-pixel/Modelwright/releases/latest"><img alt="最新版本" src="https://img.shields.io/github/v/release/chenyihang98-pixel/Modelwright?label=%E6%9C%80%E6%96%B0%E7%89%88%E6%9C%AC&amp;color=6f4bff"></a>
  <a href="https://github.com/chenyihang98-pixel/Modelwright/releases"><img alt="累计下载" src="https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fstarwright.xyz%2Fapi%2Fdownloads%2Fmodelwright&amp;query=%24.total&amp;label=%E7%B4%AF%E8%AE%A1%E4%B8%8B%E8%BD%BD&amp;suffix=%20%E6%AC%A1&amp;color=2b48f0&amp;cacheSeconds=1800"></a>
</p>

AI 生成的模型拿到手一般不能直接用：面数太高，没有 LOD 和碰撞体，尺寸和轴心不对，还得自己拖进引擎建材质、做预制体。模匠把这些接成一条线，生成、减面、绑骨、加动作、进 Unity，在一个窗口里点完。

免费。生成走云端，用你自己的 API 密钥（Tripo / Meshy / 腾讯混元），本机不用下模型权重。没有密钥也可以先用内置的演示服务把流程走一遍。

Windows 10 / 11，引擎目前只接了 Unity。

## 演示

**第二集：把大肥鱼带进三次元**　绑骨、三个动作、一键进 Unity

[![将大肥鱼带入三次元](docs/bilibili-cover-ep2.png)](https://www.bilibili.com/video/BV1YqpZ6kEw4)

<sub>大肥鱼（鲸鱼娘）是社区二创角色：原型 上善无形，女仆版二设 ZipZipPipe，设定图来自 <a href="https://github.com/TreapGoGo/deepseek-whale-girl">鲸鱼娘开源资产库</a>，CC BY-NC-SA 4.0。视频里的模型按同一协议共享。</sub>

**第一集：让纸片人站进 Unity**　一张 192 × 208 的桌宠小图，从生成到进场景

[![打破次元壁，让纸片人站进 Unity](docs/bilibili-cover.png)](https://www.bilibili.com/video/BV1VMHU6mEQt)

## 下载

到 [Releases](https://github.com/chenyihang98-pixel/Modelwright/releases/latest) 下最新版，三种任选一个：

| 文件 | |
|---|---|
| `Modelwright-Setup-…-x64.exe` | 安装版，推荐。有新版本会自动更新 |
| `Modelwright-Portable-…-x64.exe` | 便携版，单个文件。数据放在旁边的 `Modelwright-Data` 文件夹，可以装在 U 盘里带走 |
| `Modelwright-…-win.zip` | 解压就能用 |

安装包没买代码签名，第一次运行 Windows 会拦一下，点「更多信息 → 仍要运行」。不放心可以对一下 Release 页里的 SHA-256。

## 能做什么

- **生成**：图片或文字生成 3D。三视图、四视图的设定图会自动拆开，也可以让一张正面图先画成四视图再生成
- **花钱之前先检查**：提交前能看到这一单大概花多少积分，图片和参数有问题会先提醒
- **本地后处理**：减面、LOD、碰撞体、轴心和尺寸，按「资产类型 × 目标平台」的预设一次做完，不花积分
- **绑骨和动作**：云端绑骨；动作设计台里自己调待机、走、跑、跳，或者导入 Mixamo 的动作；试机场和靶场可以直接操控角色看效果
- **进 Unity**：装好插件后一键发送，材质、预制体（带 LOD 和碰撞体）、Animator 都建好，直接放进场景
- **资产库**：版本历史、文件夹、搜索、回收站，导出 GLB / OBJ / STL / PLY
- **批量**：一行写一个描述，排队生成、处理、发送，中途关掉应用也不丢

界面是中文，可以在设置里切成英文。

## 截图

| | |
|---|---|
| ![工作台](docs/screenshots/03-workspace.png) | ![预检](docs/screenshots/04-generate-preflight.png) |
| 工作台 | 提交前的检查和费用 |
| ![后处理](docs/screenshots/05-postprocess.png) | ![资产库](docs/screenshots/06-assets.png) |
| 本地后处理，前后对比 | 资产库 |
| ![绑骨与动作](docs/screenshots/08-animation.png) | ![Unity Play 模式](docs/screenshots/09-unity-play.png) |
| 绑骨和动作 | 进 Unity 后按 Play |

![星璇在 Unity 里奔跑](docs/unity-run.gif)

## 上手

1. 装好打开，跟着引导选一个生成服务。还没有密钥就选「演示（离线）」，它给的是内置的示例模型，用来熟悉流程。
2. 在首页拖一张图进去，或者写一句描述。
3. 结果在「资产」页。进「工作台」可以看网格和贴图、做后处理、绑骨、发送到 Unity。

### 填密钥

在「设置 → 生成服务」里填。

| 服务 | 密钥在哪拿 | 备注 |
|---|---|---|
| Tripo | [中国区](https://developers.tripo3d.com) / [国际区](https://developers.tripo3d.ai) | 推荐。两个区的账号和积分不通用，设置里各填各的 |
| Meshy | [meshy.ai](https://www.meshy.ai/developers/keys) | 要先订阅 Pro，免费账号的密钥用不了 |
| 腾讯混元生 3D | [TokenHub](https://console.cloud.tencent.com/tokenhub/apikey) | 先给 HY-3D 模型领免费额度或开通，再建 sk- 开头的 Key，地域选广州。应用里有带截图的指引 |

概念图和提示词优化是可选的，在「设置 → 概念图与提示词」里配，OpenAI 兼容接口、Gemini、Anthropic、DeepSeek 这些都能接。

密钥只存在你自己电脑上，用 Windows 自带的加密保存。模匠没有服务器，不收集任何数据。

生成花的是你在服务商账户里的积分。提交前会显示预计消耗，超过你设的上限要再确认一次；会扣费的请求不会自动重发。

## 连 Unity

支持 Unity 2022.3、Unity 6 和团结引擎，Built-in / URP / HDRP 都行。

在「引擎」页添加工程，点「安装插件」，之后在资产上点发送就行。编辑器开着的话会立刻导入：材质、预制体、LOD、碰撞体都建好并放进场景；带动作的角色会配好 Animator，按 Play 就能动。

没装插件也能发送，只是把文件写进 `Assets/Modelwright/`，剩下的交给 Unity 默认处理。工程里没有 glTF 导入器时，发送会问要不要装 glTFast（免费，推荐装）。

## 已知问题

- 只有 Windows 版，引擎只接了 Unity
- 主要在 Unity 6 上测，Unity 2022.3 和团结引擎测得少，遇到问题请提 Issue
- 腾讯混元的云端动作文件在 Unity 里蒙皮会撕裂，是文件本身的问题。混元绑好骨的角色，用动作设计台的「补全基础动作（本地）」来加动作
- 动作设计台的动作是程序生成的，不是动捕，做原型和试玩够用；想要更自然的就导入 Mixamo
- 裙子和头发没有布料模拟，跑起来裙摆可能穿模
- 带骨骼的模型不能在本地减面和做 LOD
- 本地抠图用的是小模型，背景复杂时边缘会有残留，可以在图片处理里手动擦
- 服务商的下载地址有时很慢。下载失败了在任务队列里点「重试」，不会重复扣费

## 数据存在哪

| | 安装版 | 便携版 |
|---|---|---|
| 资产库 | `文档\Modelwright`，可以在设置里改 | `Modelwright-Data\Library` |
| 设置、密钥、日志 | `%APPDATA%\Modelwright` | `Modelwright-Data` |

「设置 → 资产库 → 存储位置」里能看到每一处占了多少，也能一键清缓存。卸载时会问要不要连数据一起删。

## 反馈

Bug 和建议提到 [Issues](https://github.com/chenyihang98-pixel/Modelwright/issues)，写上版本号和操作步骤，最好附上日志（设置 → 语言与关于 → 打开日志，里面没有密钥）。也可以直接在 B 站视频下面留言。

## 许可

模匠免费使用，不开源，源码不公开，见 [许可协议](LICENSE.txt)（[English](LICENSE-en.txt)）。用到的第三方组件见 [THIRD-PARTY-NOTICES.txt](THIRD-PARTY-NOTICES.txt)。
