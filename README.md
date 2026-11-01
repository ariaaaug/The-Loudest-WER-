# The Loudest WER! · A little room, a little band

**团队项目说明 / Team project guide**

The Loudest WER! is a desktop-first pixel-pet music playground. Meet the White Cat, Orange Cat, and Mystery Cat, create a pet from a photo, and arrange a song together. The website runs in a browser without a build step or account.

The Loudest WER! 是一款以像素宠物和音乐创作为核心的桌面优先网页。你可以认识白猫、橘猫和神秘猫，上传照片创建宠物，并和宠物一起编曲。网站可直接在浏览器运行，无需构建项目或注册账号。

## Get the project · 获取项目

1. Open the [team repository](https://github.com/sd5913/The-Loudest-WER-). In the branch selector, choose **your own working branch** before editing. Each teammate should work on their own branch; do not assume everyone should use the same branch.

   打开上方的团队仓库，修改前在分支选择器中切换到**自己的工作分支**。每位团队成员都应在自己的分支上工作，不要默认所有人共用同一个分支。

2. For a quick preview, choose **Code → Download ZIP** and extract the complete folder. For ongoing code and asset changes, use VS Code's **Clone Git Repository** command so you can commit and sync changes to your branch.

   只想预览时，选择 **Code → Download ZIP** 并解压完整文件夹。需要持续修改代码或素材并同步到自己的分支时，请使用 VS Code 的 **Clone Git Repository（克隆 Git 仓库）**。

3. In VS Code, open the Command Palette and choose **Git: Clone**, paste the [repository link](https://github.com/sd5913/The-Loudest-WER-.git), choose a local folder, then select your branch from the branch selector. Sign in to GitHub when VS Code asks. Git must be installed on the computer.

   在 VS Code 打开命令面板，选择 **Git: Clone**，粘贴[仓库地址](https://github.com/sd5913/The-Loudest-WER-.git)，选择本地保存位置，再从分支选择器切换到自己的分支。VS Code 提示时登录 GitHub；电脑需要安装 Git。

4. Edit and preview on your own branch. In VS Code **Source Control**, review the changes, Commit, and Push / Sync to your branch. On GitHub, open a Pull Request with `main` as the target branch; after review, merge it into `main`. The team can then get the update from `main`.

   在自己的分支修改并预览。打开 VS Code 的 **Source Control（源代码管理）**检查变更、Commit，再 Push / Sync 到自己的分支。之后在 GitHub 创建目标分支为 `main` 的 Pull Request；检查通过后合并到 `main`，团队成员即可从 `main` 获取更新。

## Run locally · 本地运行

Open the project root—the folder containing `index.html` and `assets/`—in VS Code. Choose **Terminal → New Terminal**, then run the command for your system:

在 VS Code 打开项目根目录（里面应有 `index.html` 和 `assets/`），选择 **Terminal → New Terminal（新建终端）**，再按系统运行对应命令：

**macOS**
```sh
python3 -m http.server 8000
```

**Windows · PowerShell / Windows Terminal**
```powershell
py -m http.server 8000
```

Open [http://localhost:8000/](http://localhost:8000/) in the same computer's browser. Keep the terminal open while previewing; press **Ctrl + C** to stop the local server. If the terminal says port 8000 is already in use, run the same command with `8001` and open [http://localhost:8001/](http://localhost:8001/).

在同一台电脑的浏览器打开 [http://localhost:8000/](http://localhost:8000/)。预览时保持终端开启；按 **Ctrl + C** 停止本地服务。如果终端提示 8000 端口已被占用，把命令中的 `8000` 改为 `8001`，然后打开 [http://localhost:8001/](http://localhost:8001/)。

If the local link still does not open, copy the server's last few terminal lines and ask an AI assistant: **“请根据下面 VS Code 终端的实际输出，告诉我浏览器应该打开哪个 localhost 地址。如果服务没有启动，请给我适用于我当前系统的下一步操作；不要猜端口。”** Do not send passwords, tokens, or private files.

如果本地网址仍打不开，可以复制 VS Code 终端最后几行，问 AI：**“请根据下面 VS Code 终端的实际输出，告诉我浏览器应该打开哪个 localhost 地址。如果服务没有启动，请给我适用于我当前系统的下一步操作；不要猜端口。”** 不要发送密码、令牌或私人文件。

The first time you play audio, click **Play together** once to enable browser audio. Assets do not need a separate installation; download or clone the entire project and keep `assets/` in place.

第一次播放声音时，点击一次 **Play together（一起演奏）**以启用浏览器音频。素材不需要单独安装；请下载或克隆完整项目，并保留 `assets/` 文件夹。

## Pages · 网站页面

| Page 页面 | English | 中文 |
|---|---|---|
| `index.html` | Interactive home room, Sunset/Night themes, draggable cats, and quick links to other pages. | 互动首页，可切换黄昏/夜晚主题、拖动猫咪，并进入其他页面。 |
| `pets.html` | Create a pet from a photo, record/upload a voice, preview the pixel effect, and adopt a pet. | 上传照片创建宠物、录制或上传声音、预览像素效果及领养宠物。 |
| `studio.html` | Select pets and sounds; adjust Volume, Pitch, Rhythm, and Repeat; choose templates; play, pause, and save music. | 选择宠物和叫声，调节音量、音高、节奏与重复，选择模板并播放、暂停和保存音乐。 |
| `collection.html` | Reopen or remove music saved in this browser. | 打开或移除此浏览器中保存的音乐。 |
| `gallery.html` | Browse the project's pet characters and example sounds. | 浏览项目宠物角色和示例声音。 |

## Replaceable assets · 替换素材

Keep the existing path and filename when replacing an asset. In VS Code, open the matching file in `assets/`, back up the original, replace it with the new file, and refresh the browser. To share the change, review and commit it in VS Code Source Control, Push it to your own branch, then open a Pull Request to `main` and merge after review.

替换素材时尽量沿用原有路径和文件名。在 VS Code 打开 `assets/` 中对应文件，先备份，再替换并刷新浏览器查看。要让团队看到修改，请在 VS Code 的 Source Control（源代码管理）检查并 Commit，再 Push 到自己的分支，创建目标为 `main` 的 Pull Request，检查通过后合并。

| Content 内容 | Location 路径 | Notes 注意事项 |
|---|---|---|
| Home backgrounds / 首页背景 | `assets/backgrounds/home-sunset.png`, `home-night.png` | Keep the original ratio. The computer is part of each background. / 保持原图比例；电脑已包含在背景图中。 |
| Home cats / 首页猫咪 | Matching transparent PNGs in `assets/pets/`; night files include `-night`. / `assets/pets/` 中对应的透明 PNG，夜晚版本文件名带 `-night`。 | Keep canvas and subject placement similar to avoid misalignment. / 保持画布和主体位置相近，避免错位。 |
| Studio background / 工作室背景 | `assets/backgrounds/seaside-park.png` | Keep the filename and folder. / 保留原文件名和目录。 |
| Example sounds / 示例声音 | WAV files in `assets/sounds/` | Keep WAV format and filename. / 保持 WAV 格式和文件名。 |
| Home logos and buttons / 首页 Logo 与按钮 | `assets/wer-christmas-ui/` | Keep the transparent edges; button canvases are 300 × 100 px. / 保留透明边缘；按钮画布为 300 × 100 像素。 |

## Main code · 主要代码

| Files 文件 | Purpose 用途 |
|---|---|
| `index.html`, `home.js`, `experience.css` | Home layout and interactions / 首页布局与互动 |
| `pets.html`, `pets.js`, `pet-art.js`, `store.js` | Pet creation, voice input, and adoption / 宠物创建、声音输入与领养 |
| `studio.html`, `app.js` | Music editor and playback / 音乐编辑与播放 |
| `collection.html`, `collection.js`, `store.js` | Saved music / 已保存音乐 |
| `theme.js`, `style.css`, `pixel-ui.css`, `experience.css` | Shared themes and visual styles / 全站主题与视觉样式 |

## Saving and sharing · 保存与分享

Music, adopted pets, and custom pet details are stored in the current browser only; they do not automatically sync across devices. **Share** copies a local studio URL. It does not upload a song or create a public link. This prototype has no account system, cloud sync, or server-side storage.

音乐、领养宠物和自定义宠物资料仅保存在当前浏览器，不会自动同步到其他设备。**Share（分享）**复制的是本地工作室网址，不会上传歌曲，也不会生成公开链接。本初版没有账号系统、云端同步或服务器存储。

For page descriptions and control explanations, see [Website Function Guide / 网站功能说明（Word）](docs/网站功能说明.docx). For branches, local setup, collaboration flowcharts, and asset replacement steps, see [Team Collaboration and Asset Guide / 团队协作与素材替换说明（Word）](docs/团队协作与素材替换说明.docx).

页面与控件说明见[网站功能说明（Word）](docs/网站功能说明.docx)；分支协作、本地运行、流程图和素材替换步骤见[团队协作与素材替换说明（Word）](docs/团队协作与素材替换说明.docx)。

The current product direction is recorded in [`SPEC.md`](SPEC.md). / 当前产品方向见 [`SPEC.md`](SPEC.md)。
