# Potat0's DN42 Network

> If you are already on the DN42 network and have DNS configured, try visiting the DN42 domain of this page:
>
> 如果你已经加入 DN42 网络并且配置了 DNS，不妨试试访问本页在 DN42 中的域名：
>
> [https://potat0.dn42/](https://potat0.dn42/)
> 
> You need to configure DN42 DNS to access `.dn42` domain names. Please check [this Wiki](https://dn42.dev/services/DNS).
> 
> 你需要配置 DN42 DNS 才能访问 `.dn42` 域名。请查看[此 Wiki](https://dn42.dev/services/DNS)。

## Basic Information 基本信息

- ASN: `AS4242421816`

- DN42 IPv4: `172.23.246.0/26`

- DN42 IPv6: `fd2c:1323:4042::/48`

- Domain: `potat0.dn42`

### Contact 联系方式

Want peer or any other situation? Feel free to contact me! 想要 Peer 或是其他任何情况？欢迎随时联系我！

- Telegram: **Preferred! 首选！**

  [@Potat0_PM_Bot](https://t.me/Potat0_PM_Bot)

- Email:

  dn42 {at) potat0 [dot} cc
  
I'll attempt to keep checking my inbox at least 2 times a day, but there is definitely a big lag. So contact me on Telegram if possible.
  
我将尝试每天至少检查 2 次收件箱，但这肯定有不小的延迟。因此如果可能的话，建议优先选择在 Telegram 上联系我。

## AutoPeer & Bot 自动对等连接与机器人

I maintain a Telegram bot to provide the AutoPeer service and some basic DN42 network services (e.g. `ping`, `traceroute`, `rank`).  我维护了一个 Telegram 机器人，用于提供 AutoPeer 服务及一些基本的 DN42 网络服务（如 `ping`、`traceroute`、`rank`）。

You can find it at [@Potat0_DN42_Bot](https://t.me/Potat0_DN42_Bot), and feel free to add it to your group chat. 你可以在 [@Potat0_DN42_Bot](https://t.me/Potat0_DN42_Bot) 找到它，也欢迎你将它添加至群聊。

The bot is open source [here](https://github.com/Potat0000/dn42-bot). If you like it, feel free to deploy it yourself and Star! 机器人在 [此处](https://github.com/Potat0000/dn42-bot) 开源。如果你喜欢的话也可以自己部署。欢迎 Star！

## Looking Glass

I provide a Looking Glass service at the following address. 我在以下地址提供了 Looking Glass 服务。

- [https://lg.dn42.potat0.cc/](https://lg.dn42.potat0.cc/) (Clearnet 公网)
- [https://lg.potat0.dn42/](https://lg.potat0.dn42/) (DN42)

## Status Page

I provide a Status Page at the following address. 我在以下地址提供了一个状态页。

- [https://status.dn42.potat0.cc/](https://status.dn42.potat0.cc/) (Clearnet 公网)
- [https://status.potat0.dn42/](https://status.potat0.dn42/) (DN42)

## Requirements 要求

- For now, I only accept tunnel connections using WireGuard. My WireGuard AllowedIPs are as follow. 目前，我只接受使用 WireGuard 的隧道连接。我的 WireGuard AllowedIPs 如下。

  ```
  AllowedIPs = 172.20.0.0/14, 10.0.0.0/8, 172.31.0.0/16, fd00::/8, fe80::/64
  ```
  
- My network only accepts routes that are registered in DN42, and unknown routes (to accomodate newly registered users). 我的网络只允许接收在 DN42 中注册过的路由，以及未知路由（以方便新注册 DN42 的用户）。

- Contact information in the registry must always be up to date and admins must respond when contacted. 在注册处的联系信息必须是有效的，且管理员在需要的时候可以联系得到。

- I do not Peer with servers in mainland China, but I don't completely refuse either. If your server is in mainland China and you have a reasonable explanation, please contact me directly. 我不与中国大陆服务器进行 Peer，但是也不完全拒绝。如果你的服务器在中国大陆，并且有合理理由，请直接联系我。

## Peeeing requests for manual peering 人工对等互联请求

**Please use the AutoPeer service first! 请优先使用 AutoPeer 服务！**

If you are unable to use the AutoPeer service, then please send a Peer Request as follows. 如果你无法使用 AutoPeer 服务，则请按如下要求发送 Peer Request。

- The node you want to peer. 你想要对等互联的节点。

- Your WireGuard public key. 你的 WireGuard 公钥。

- The WireGuard endpoint for me to connect. Let me know if it's dynamic or you don't have one. 我要连接到的 WireGuard 公网信息。如果是动态的或者你没有公网地址，记得告诉我。

- Your ASN. 你的 ASN。

- The session(s) to use: IPv6 + IPv4, IPv6 only, or IPv4 only. 要使用的会话：IPv6 + IPv4，仅 IPv6，或仅 IPv4。

- The extra capabilities: Multiprotocol BGP / Extended next hop / Extended messages. 额外的能力：Multiprotocol BGP / Extended next hop / Extended messages。

- The IP address(es): One for each session, and an additional IPv4 if you use MP-BGP without ENH. IP 地址：每个会话只需要一个，如果你用 MP-BGP 且不用 ENH，则同时需要 IPv6 和 IPv4 地址。

E.g.:
```
Node: US1
Public key: xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Endpoint: your.domain.tld:21816
ASN: 4242421816
Sessions: IPv6 + IPv4
Capabilities: MP-BGP, ENH
IPv6: fe80::1816
IPv4: None
```

## Nodes 节点

Setting up a peering in every region where we both have nodes is recommended to improve network robustness.

推荐在每个我们都有节点的地区建立 Peer，以加强网络健壮性。

### US1 | New York, USA | BuyVM

- Endpoint 公网地址

  `us1.dn42.potat0.cc`

  `198.98.56.83`

  `2605:6400:10:ffc:de30:1d96:e61e:43ff`
  
- DN42

  `172.23.246.1`
  
  `fd2c:1323:4042::1`
  
  `fe80::1816`

- WireGuard Public Key

  `LUwqKS6QrCPv510Pwt1eAIiHACYDsbMjrkrbGTJfviU=`

- Connectivity 连接性
  
  IPv4 + IPv6 (5Gbps)
  
### JP1 | Tokyo, Japan | AWS

- Endpoint 公网地址

  `jp1.dn42.potat0.cc`

  `35.75.89.80`

  `2406:da14:965:c400:3ef9:6344:5f16:be2`

- DN42

  `172.23.246.2`
  
  `fd2c:1323:4042::2`
  
  `fe80::1816`

- WireGuard Public Key

  `Tv1+HniELrS4Br2i7oQgwqBJFXQKculsW8r+UOqQXH0=`

- Connectivity 连接性
  
  IPv4 + IPv6 (500Mbps)
  
### NO1 | Sandefjord, Norway | Terrahost

- Endpoint 公网地址

  `no1.dn42.potat0.cc`

  `185.125.171.92`

  `2a03:94e0:ffff:185:125:171::92`

- DN42

  `172.23.246.3`
  
  `fd2c:1323:4042::3`
  
  `fe80::1816`

- WireGuard Public Key

  `H6HdsuQsav9puKyo8SJaML0vPU/a2lLQjTRc7dmiqjs=`

- Connectivity 连接性
  
  IPv4 + IPv6 (10Gbps)
