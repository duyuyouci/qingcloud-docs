---
title: "查看集群信息"
description: 本小节主要介绍如何查看 ClickHouse 集群信息。 
keywords: ClickHouse 集群信息
weight: 10
collapsible: false
draft: false
---


ClickHouse 集群创建成功后，可在 AppCenter 查看集群信息，包括集群基本属性、服务端口信息、租赁信息、节点信息、配置参数、告警配置、备份信息、角色详情等。

本小节主要介绍如何查看集群信息。

## 前提条件

- 已获取 QingCloud 管理控制台登录账号和密码，且已获取集群查看权限。

## 操作步骤

1. 登录 QingCloud 管理控制台。
2. 选择**产品与服务** > **数据仓库与 BI** > **ClickHouse**，进入集群管理页面。

   可查看当前区域集群列表，以及集群基本信息。

    <img src="../../../_images/cluster.png" alt="集群列表" style="zoom:100%;" />

3. 选择目标集群，点击目标集群 ID，进入集群详情页面。

    可查看集群各详细信息，以及执行集群的各项功能管理操作。

4. 当在对集群执行操作后，可在集群详情页面左下侧，查看集群操作日志。

   <img src="../../../_images/operate_log.png" alt="操作日志" style="zoom:50%;" />

### 基本属性

在集群详情页面左侧**基本属性**区域，可查看集群基本状态、版本信息、节点数量、网络信息等。

点击下拉栏图标，展开集群操作列表，可查看集群服务功能。

<img src="../../../_images/basic_info.png" alt="基本属性" style="zoom:50%;" />

### 服务端口信息

在集群详情页面左侧**连接信息**区域，可查看集群服务端口、高可用读写 IP等。

- 高可用 IP：内网访问高可用 IP。

> **注解**
> 
> 由于集群采用无主构架，建议直接使用节点 IP 管理集群，以便可以更加灵活的控制集群的负载。

<img src="../../../_images/check_access_info.png" alt="连接信息" style="zoom:50%;" />

### 节点

在**节点**页面，可查看集群各节点的 ID、服务状态、监控信息、资源配置等。通过节点任意 IP，可对集群进行管理操作。

<img src="../../../_images/check_node.png" alt="节点" style="zoom:100%;" />

### 配置参数

在**配置参数**页面，可查看集群性能优化配置参数项。

![配置参数](../../../_images/config_list.png)

### 告警

在**告警**页面，可以查看集群告警配置信息，及时掌握集群的资源和服务状况。

![监控告警](../../../_images/alarm_list.png)

### 备份

在**备份**页面，可以查看集群节点备份状态。

![备份状态](../../../_images/backup_info.png)

### 用户列表

在**用户列表**页面，可以查看集群用户账号列表信息。

<img src="../../../_images/account_list.png" alt="用户列表" style="zoom:50%;" />

### 租赁信息

在集群详情页面左侧**租赁信息**区域，可以查看集群当前计费信息。

<img src="../../../_images/payment_info.png" alt="租赁信息" style="zoom:50%;" />
