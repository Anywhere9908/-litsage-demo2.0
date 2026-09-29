# 览卷 · LitSage 静态演示站（GitHub Pages 版）

单文件、纯前端、零依赖的 LitSage 演示站。内含**交互式前端 mock**（五环闭环动画、主张—证据表、
合规核验、Evidence Trace、留痕台账）与**作品展示视频录制脚本浮层**。
可直接拖到任意静态托管，**最快 1 分钟拿到一个可展示网址**。

---

## 一、本地预览（最快）

直接双击 `index.html` 即可在浏览器打开。或起一个本地服务：

```bash
cd static-site
python3 -m http.server 8080
# 打开 http://127.0.0.1:8080
```

---

## 二、部署到 GitHub Pages（拿到公开网址）

1. 新建一个 GitHub 仓库，例如 `litsage-demo`。
2. 把 `index.html`（以及本 README）上传到仓库根目录。
   - 网页操作：仓库页点 **Add file → Upload files** 拖入 `index.html` → Commit。
   - 命令行：
     ```bash
     git init
     git add index.html README.md
     git commit -m "LitSage demo"
     git branch -M main
     git remote add origin https://github.com/<你的用户名>/litsage-demo.git
     git push -u origin main
     ```
3. 进入仓库 **Settings → Pages**。
4. Source 选 **Deploy from a branch**，Branch 选 `main`，目录选 `/ (root)`，Save。
5. 等待 1–2 分钟，访问：
   ```
   https://<你的用户名>.github.io/litsage-demo/
   ```
   这个网址即可用于作品展示、二维码、报名表。

> 若希望仓库根即是站点，可把 `index.html` 放到名为 `<用户名>.github.io` 的仓库，则网址为
> `https://<用户名>.github.io/`。

---

## 三、部署到其它静态托管

- **Netlify / Vercel**：直接拖拽 `static-site` 文件夹到其部署面板，秒级上线。
- **Gitee Pages / 腾讯云 / 阿里云 OSS**：把 `index.html` 上传到静态网站目录，开启静态托管即可。

---

## 四、演示脚本在哪

页面右下角 **「📋 演示脚本」** 按钮，点开即是完整的 4 分 30 秒视频录制分镜脚本
（时间轴 / 画面 / 旁白），录制时可直接对照。

---

## 五、与 Python 版的区别

| | 静态站（本站） | Python 版 |
|---|---|---|
| 依赖 | 无 | Flask |
| 引擎 | 内置 JS mock | `engine.py` |
| 部署 | GitHub Pages | 本地/服务器 |
| 用途 | 拿展示网址、录视频 | 本地跑通、答辩演示 |

两者**引擎逻辑完全一致**，展示效果相同。

---

Created By 闻道