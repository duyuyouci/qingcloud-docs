---
title: "创建备份"
description: 本小节主要如何创建 PostgreSQL 数据备份。 
keywords: PostgreSQL 数据备份；
weight: 10
collapsible: false
draft: false
---



在 AppCenter 集群管理控制台，PostgreSQL 提供数据备份管理，可以通过**备份**服务来管理集群数据。

PostgreSQL 集群硬盘可以创建多条备份链，每条备份链可包括一个**全量备份**和多个**增量备份**，支持从任意备份点恢复数据。

集群备份创建成功后，可基于备份创建一个新集群恢复数据，更多集群备份管理说明，请参见[备份](../../../../../storage/backup/)。

本小节主要介绍如何创建 PostgreSQL 集群备份。

## 约束限制

- 备份只能捕获已经写入磁盘的数据，不能捕获缓存里的数据。
- 仅备份主实例的主节点。

## 前提条件

- 已获取 QingCloud 管理控制台登录账号和密码，且已获取集群操作权限。
- 已创 PostgreSQL 集群状态为**活跃**。

## 操作步骤

1. 登录 QingCloud 管理控制台。
2. 选择**产品与服务** > **数据库与缓存** > **关系型数据库 PostgreSQL**，进入集群管理页面。
3. 选择目标集群，鼠标右键展开集群快速操作列表。
4. 点击**创建备份**或在备份链上新增备份，弹出备份提示窗口。

   <img src="../../../_images/backup_notice.png" alt="备份提示" style="zoom:50%;" />

5. 点击**继续**，配置备份信息。

    输入备份名称，以及勾选**创建新备份链接**。

   <img src="../../../_images/backup_config.png" alt="备份配置" style="zoom:50%;" />

6. 确认参数信息无误后，点击**保存**，返回备份列表页面。

   待集群状态切换为**活跃**，即创建集群当前备份完成。

    <img src="../../../_images/backup_list.png" alt="备份列表" style="zoom:100%;" />

备份创建成功后，可从备份节点创建新集群，恢复集群信息。

![恢复集群](../../../_images/pg_restore.png)
