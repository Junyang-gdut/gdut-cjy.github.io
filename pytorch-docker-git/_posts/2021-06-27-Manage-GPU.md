---
layout: post
title: 【Git】Manage GPU
---

1. **查看指定进程使用命令**

   ```
   ps -f -p *
   ```

2. **批量清理显卡中残留进程**

   ```
   sudo fuser -v /dev/nvidia* |awk '{for(i=1;i<=NF;i++)print "kill -9 " $i;}' | sudo sh
   ```

3. **查看指定显卡占用进程**

   ```
   fuser -v /dev/nvidia*
   ```

   


