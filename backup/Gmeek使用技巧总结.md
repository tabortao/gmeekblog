## 快速搭建

根据[Gmeek快速上手](https://blog.meekdai.com/post/Gmeek-kuai-su-shang-shou.html)，可以快速完成自己Blog的搭建。

## 插件使用

参考[【Gmeek进阶】插件功能的使用
](https://blog.meekdai.com/post/%E3%80%90Gmeek-jin-jie-%E3%80%91-cha-jian-gong-neng-de-shi-yong.html#vercount)，对Blog添加一些插件。
- 增加灯箱插件、TOC目录插件、Vercount统计插件；
- config.json最后不能有标点符号，如何“,”。
```json
{
    "title":"可持续学园",
    "subTitle":"热爱生活、喜欢分享。",
    "avatarUrl":"https://github.githubassets.com/favicons/favicon.svg",
    "GMEEK_VERSION":"last",
    "script":"<script src='https://blog.meekdai.com/Gmeek/plugins/GmeekTOC.js'></script><script src='https://blog.meekdai.com/Gmeek/plugins/lightbox.js'></script>",
    "allHead":"<script src='https://blog.meekdai.com/Gmeek/plugins/GmeekVercount.js'></script>"
}
```

## 部署到Cloudflare

> 对于极致的简洁和 GitHub 生态的深度集成，选择 GitHub Pages。对于更高的性能、更强大的自动化构建能力和边缘计算扩展性，选择 Cloudflare Pages。Cloudflare全球CDN，极致加速，性能更优。对于一个专业的静态站点项目，尤其是有一定用户访问量和扩展需求时，Cloudflare Pages 通常是更现代和强大的选择。对于一个随性的个人博客或开源项目文档，GitHub Pages 的简单性则无可匹敌。
- 登录[Cloudflare](https://dash.cloudflare.com/)
- 点击“计算(Workers)-Workers和Pages”，创建Pages，选择导入github里面创建的blog
- 因为项目已经使用Github Action自动构建好了，Cloudflare Pages无需构建命令，因此这里构建配置需要注意：构建命令为空；构建输出填写“docs”,对应仓库中docs文件夹。（这里我没有配置正确，导致Cloudflare Pages部署后的域名无法访问）
<img width="913" height="300" alt="Image" src="https://github.com/user-attachments/assets/14dab828-5bf7-4865-9c32-ce0eedfb53b3" />
- 点击部署，部署后设置自定义域名，注意需要在自己的域名解析中，记录类型选择CNAME，主机记录填写“blog”等自己想要的二级域名。
- Cloudflare会自动给域名添加SSL证书，形成很强的防护。

## 高级使用方法
详见作者官网[Gmeek合集](https://blog.meekdai.com/tag.html#Gmeek)