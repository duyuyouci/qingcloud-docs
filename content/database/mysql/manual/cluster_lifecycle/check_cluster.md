---
title: "查看集群信息"
description: 本小节主要介绍如何查看 MySQL Plus 集群信息。 
keywords: mysql plus 集群信息
weight: 10
collapsible: false
draft: false
---


MySQL Plus 集群创建成功后，可在 AppCenter 查看集群信息，包括集群基本属性、连接信息、租赁信息、节点信息、配置参数信息、告警配置、节点状态、服务地址、灾备关系、用户账号等。

本小节主要介绍如何查看集群信息。

## 前提条件

- 已获取 QingCloud 管理控制台登录账号和密码，且已获取集群查看权限。

## 操作步骤

1. 登录 QingCloud 管理控制台。
2. 选择**产品与服务** > **数据库与缓存** > **关系型数据库 MySQL Plus**，进入集群管理页面。

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

### 连接信息

在集群详情页面左侧**连接信息**区域，可查看集群服务端口、高可用读写 IP、外网地址、IP 白名单等。

- 高可用读 IP：内网访问高可用读 IP。可将请求在所有节点之间进行负载分担，提高读取性能，消除单点故障。

- 高可用写 IP：内网访问高可用写 IP。始终指向 Master 节点。

- 高可用 Proxy IP：始终指向 Proxy 实例的 Master 节点。

> **注意**
> 
> -务必使用读 IP 执行读请求，以将所有读请求按轮询方式分摊到所有节点.
> 
> -务必使用写 IP 执行写请求，以保证切主后不影响业务。
> 
> -**Proxy 实例**用于读写分离。Proxy IP 作为集群预留 IP ，如未创建用 **Proxy 实例**该 IP 仍然被占用但是无法访问。

- 外网地址：开启外网访问后，可通过外网地址连接数据库。

- IP 白名单：开启外网访问后，允许通过外网地址访问数据库的服务器 IP 地址。

<img src="../../../_images/check_access_info.png" alt="连接信息" style="zoom:50%;" />

### 节点列表

在**节点**页面，可查看集群各节点的 ID、服务状态、监控信息、资源配置等。

![节点](../../../_images/check_node.png)

### 配置参数

在**配置参数**页面，可查看集群性能优化配置参数项。包括可以修改并持久化的配置参数，未标注会重启服务的参数，可以运行时修改，对服务无影响。

> **注解**
> 
> 修改后将导致自动重启集群的参数，请在业务低峰时进行修改。

![配置参数](../../../_images/config_list.png)

### 监控告警

在**告警**页面，可以查看集群告警配置信息，及时掌握集群的资源和服务状况。

![监控告警](../../../_images/alarm_list.png)

### 备份

在**备份**页面，可以查看集群备份列表信息，可查看集群列表和**备份链**结构示意图，以及可从备份创建新集群。

![备份信息](../../../_images/backup.png)

### 节点状态

在**节点状态**页面，可以查看集群主实例的节点状态、角色信息。主要用于区分主节点主备状态。

> **注解**
> 
> `基础版`集群为单节点，不区分主备节点，因此不支持查看节点状态。

![节点状态](../../../_images/display_nodeinfo.png)

### 服务地址

在**服务地址**页面，可以查看集群节点日志服务地址。开启日志服务端后，可通过服务地址登录 HTTP 服务预览和下载 MySQL Plus 数据库节点日志，

<img src="../../../_images/log_server_addr.png" alt="日志服务地址" style="zoom:50%;" />

### 灾备关系

在**服务地址**页面，可以查看集群灾备信息。需在开启集群灾备后，才可获取关联灾备集群的信息。

<img src="../../../_images/disaster_recover.png" alt="灾备信息" style="zoom:50%;" />

### 账号列表

在**服务地址**页面，可以查看集群除运维账号外的 MySQL 账号。

![账号](../../../_images/check_user.png)

### 租赁信息

在集群详情页面左侧**租赁信息**区域，可以查看集群当前计费信息。

<img src="../../../_images/payment_info.png" alt="租赁信息" style="zoom:50%;" />
