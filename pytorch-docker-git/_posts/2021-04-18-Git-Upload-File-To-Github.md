---
layout: post
title: 【Git】Using Git upload file to Github
---

1. **建立git仓库，cd到你的本地项目根目录下，执行git命令**

   ```
   git init
   ```

2. **将项目的所有文件添加到仓库中**

   ```
   git add *
   ```

3. **将add的文件commit到仓库**

   ```
   git commit -m "注释"
   ```

4. **上传github之前，要先pull一下，再push到main分支**

   ```
   git pull
   git push -u origin main
   ```

   

