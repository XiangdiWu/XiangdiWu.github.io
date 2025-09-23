
# 常规目录结构
.<br>
├── archetypes # 存放生成博客的模版<br>
├── assets # 存放被 Hugo Pipes 处理的文件<br>
├── config # 存放 hugo 配置文件 支持 JSON YAML TOML 三种格式配置文件<br>
├── content # 存放 markdown 文件<br>
├── data # 存放 Hugo 处理的数据<br>
├── layouts # 存放布局文件<br>
├── static # 存放静态文件 图片 CSS JS文件<br>
└── themes # 存放主题<br>

# 使用方法

## 项目git配置

✅ 通过git clone获取项目<br>
git clone https://github.com/XiangdiWu/xiangdiwu.github.io.git<br>

✅ 理解通过git同步内容<br>
    - 理解 .gitignore 文件<br>
    - 理解 .gitmodules 文件，如何修改？<br>
    - git 流程中需要注意的事情？<br>
    - github 需要进行什么配置？<br>


✅ 项目内 git 配置（可选）：<br>

    ```bash

    git config user.name "XiangdiWu"

    git config user.email "bernicewu3@gmail.com"

    ```

✅ 设置代理（可选）：<br>

    ```bash
    git config --global http.proxy http://127.0.0.1:7890

    git config --global https.proxy https://127.0.0.1:7890

    ```

✅ 设置 git 子模块（可选）：<br>

    ```bash
    git submodule add https://github.com/appernetic/hugo-nederburg-theme themes/hugo-nederburg-theme

    git submodule add https://github.com/XiangdiWu/hugo-theme-cleanwhite-modify.git themes/hugo-theme-cleanwhite

    git submodule add https://github.com/XiangdiWu/blog_img.git static/img

    git submodule add https://github.com/XiangdiWu/blog_slides.git static/slides

    ```
❗️ 先提交子模块内容，再提交父项目内容：<br>

## 构建 Make 管理文件方式（可选）

✅ 配置 Make 环境（MacOs）：
    
    ```bash
    brew install make
    ```

✅ 使用 Makefile 构建项目：
    - 理解 Make 文件的作用<br>
    - 理解 Make 文件中的内容<br>

    运行 Make 文件（默认执行第一个任务，即 serve）：
    
    ```bash
    make
    ```
    执行其他任务，可以指定：
    
    ```bash
    make index-algolia
    ```

## 博客配置（初级）

config.yaml 配置：<br>
    - ✅ 修改个人介绍<br>
    - ✅ 修改个人头像/照片<br>
    - ✅ 修改个人社交账号<br>
    - ✅ 修改个人邮箱<br>
    - ✅ 修改 Quick Links<br>
    - ✅ 修改 Publications<br>
    - ✅ 删除他人cotent<br>
    - ✅ 添加自己的content（示例）<br>
    - 其他<br>

修改 static/img/reward/ 文件夹中的内容<br>  
    - ✅ 修改static/img/reward/ 文件夹中的图片<br>
    - ✅ 修改static/img/favicon.ico 文件<br>
    - ✅ 修改static/ads.txt 文件<br>

## 完善配置（进阶）

✅ 设置评论区：giscus<br>
    - 教程参考：https://www.heyjude.blog/zh-cn/posts/giscus-comments-hugo/<br>
    - giscus：https://giscus.app/zh-CN<br>
    （需要知道github仓库链接）

✅ 设置搜索功能 algolia：<br>
    - 教程参考：https://ieblyang.github.io/hugo-algolia/<br>
    - algolia：https://www.algolia.com/<br>
    - 坑点提示：https://juejin.cn/post/7228692613037277221<br>
    （不需要知道github仓库链接）

❗️ 极简示例：<br>

    ```bash

    hugo # 生成页面和索引文件

    npm init

    npm install atomic-algolia --save

    # 配置 .env 
    
    npm run algolia

    hugo server

    ```

✅ 设置博客托管<br>
    - 这个项目是用什么托管的？<br>
    - 如何设置托管？<br>
    - 为什么托管不成功？<br>
    - Github pages：https://hugo.opendocs.io/zh-cn/hosting-and-deployment/hosting-on-github/<br>
    - Netlify pages：https://hugo.opendocs.io/zh-cn/hosting-and-deployment/hosting-on-netlify/<br>
    - Cloudflare Pages：https://www.heyjude.blog/zh-cn/posts/deploy-hugo-to-cloudflare/<br>

✅ 修改域名<br>
    - 注册阿里云或腾讯云账号，任选一家购买域名
    - 实名认证，等待审核
    - 在阿里云管理域名：控制台-->进入域名管理界面-->邮箱验证-->模版实名认证-->域名实名认证-->等待平台审核-->等待注册局审核-->查看审核结果
    - 进入解析添加记录：CNAME、@、默认、记录值：xiangdiwu.github.io
    - 

**还有什么其他需要配置的内容？**

✅ 设置 google analytics：<br>
    - 注册 google analytics 账号<br>
    - google analytics：https://analytics.google.com/<br>
    - 添加网站和数据流<br>
    - condig.yaml 设置 google analytics 的 id<br>

✅ 清空或删除文件内容： static/ads.txt<br>

## hugo 博客内显示 LaTex 公式和 mermaid 图表

❌ 修复 Latex 和 KaTeX 的显示问题：<br>
    - 理解 static/js/katex.min.js 文件的作用<br>

✅ mermaid 图表：<br>
    - layouts/partials/mermaid.html 文件的作用<br>
    - layouts/post/single.html 文件的作用<br>

## 添加文章以及博客本地预览

✅ 添加博客文章：<br>
    - 添加文章(post文件夹，layout：post，categories：[Life]，导航栏会出现 Life)<br>
    - 修改 about 页面<br>
    - 修改 reading 页面<br>
    - 修改 travel 页面<br>

❗️ 调试项目时，每一次增添文章或修改文章后，都要进行下面步骤：<br>
    - （可选）删除 public<br>
    - 生成页面和索引文件：hugo<br>
    - 将索引文件上传：npm run algolia<br>
    - 在网页查看博客：hugo server<br>
❗️ 待完成部署后只需要 git 即可：<br>
❗️ 先提交子模块内容，再提交父项目内容：<br>