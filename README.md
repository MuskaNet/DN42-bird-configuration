# DN42 Configuration Template

DN42 节点基本配置模板。

## 主要配置

- local/
  - own.conf `定义本机信息`
  - rpki.conf `定义 RPKI Server`
- peers/
  - .template.conf `MBGP 模板`
- ospf/ `OSPF 区域配置`

## 主路由和边缘路由接口定义

主路由接口全部使用 `master<ID>` 命名  
边缘路由接口全部使用 `edge<ID>` 命名

## 关于协议

### OSPF

IPv4 均采用 OSPFv2 协议  
IPv6 均采用 OSPFv3 协议

### MBGP

默认模板为 IPv4 开启扩展下一跳，修复 OpenWrt 等系统安装的 Bird2 默认禁用扩展下一跳导致路由写入失败
