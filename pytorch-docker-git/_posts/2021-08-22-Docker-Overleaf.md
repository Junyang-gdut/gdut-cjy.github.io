---
layout: post
title: 【Git】Docker Overleaf
---

最近在学校连接Overleaf经典掉线，可能是AAAI要截稿服务器比较炸的原因。后面发现Overleaf是开源的[Github](https://github.com/overleaf/overleaf)，便搜了一下本地部署Overleaf的教程，主要是利用Docker

1. **Docker拉取已经配置好Texlive2020的镜像**

   ```
   docker pull kingsleyluoxin/sharelatex:full
   ```

2. **运行Docker，其中8080为端口号**

   ```
   docker run -p 8080:80 -d kingsleyluoxin/sharelatex:full
   ```

3. **通过浏览器访问 http://localhost:8080/launchpad 可直接配置管理员用户**

   ------

   备注：

   1. **检查端口状态**

      ```
      sudo firewall-cmd --query-port=8080/tcp
      ```

   2. **开放端口**

      ```
      sudo firewall-cmd --permanent --add-port=8080/tcp
      ```