# 薛牛牛律师事务所 · 本地演示

启动：在本目录运行 `node server.js`，浏览器访问 http://127.0.0.1:5173 。无需安装依赖。

支持中文/英文切换，语言选择保存在浏览器中。页面采用哈希路由，便于后续部署到静态托管平台。所有内容数据集中在 app.js，样式在 style.css。

这是参考恒和信网站栏目组织制作的第一版演示，并非像素级复刻。机构资料、律师人物、合作客户及联系方式均为虚构。咨询表单不会发送或保存信息。上线前需替换真实资料、核实资质并配置正式联系方式。

配图：Unsplash（城市、办公及会议空间示意），已下载至 assets，网站运行无需外部图片服务。示例地址中不存在真实的地图定位。尚未连接后台、邮箱、GitHub 或部署平台。

## GitHub / Sealos 部署
GitHub Actions 在 main 分支更新时构建 Nginx 镜像至 GHCR，发布 latest 和提交 SHA 两类标签。
Sealos 应用管理使用镜像 `ghcr.io/charlestzqtzq-bit/xue-niuniu-law:<commit-sha>`，容器端口 80，启用 HTTPS 公网访问。
GitHub 仓库公开不代表容器镜像自动公开；首次构建完成后需确认 Package 的访问权限，或在 Sealos 配置私有镜像拉取认证。
此工作流只构建镜像，不自动更新 Sealos。后续版本需在 Sealos 修改镜像标签后部署。
