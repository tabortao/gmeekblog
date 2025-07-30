> 刚开始玩网站的时候，使用的是阿里云域名提供的DNS，玩了1年多，之前知道Cloudflare更好些，但是一直懒得折腾，最近有空，折腾起来。

## 修改阿里云DNS

- 在阿里云控制台，选择：域名与网站—域名列表，在自己域名最右侧，点击管理。
- DAN管理-DNS修改，修改为Cloudflare提供的。

## 申请Cloudflare API Token

- 进入 [Cloudflare 官网](https://dash.cloudflare.com/) → 选择你的域名。
- 右上角用户头像 → 「我的个人资料（My Profile）」 → 「API Token」（或直接访问：[CF API Tokens](https://dash.cloudflare.com/profile/api-tokens)）。
- 点击「创建 Token」 → 选择「Edit zone DNS」模板
- 点击 「继续到摘要」 → 「创建 Token」 → 复制 Token（⚠️ 你只会看到这一次！建议妥善保存）

## DNS 托管

- 在Lucky等平台，设置DNS服务商为Cloudflare。 