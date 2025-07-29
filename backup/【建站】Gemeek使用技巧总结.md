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
