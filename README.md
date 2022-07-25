# Potat0's DN42 Network

> If you are already on the DN42 network and have DNS configured, try visiting the DN42 domain of this page:
>
> 如果你已经加入 DN42 网络并且配置了 DNS，不妨试试访问本页在 DN42 中的域名：
>
> [https://potat0.dn42/](https://potat0.dn42/)
>
> If you are experiencing certificate issues, it may mean that your device does not trust the DN42 root certificate. Please check [this Wiki](https://dn42.dev/services/Certificate-Authority).
>
> 如果你遇到了证书问题，可能意味着你的设备没有信任 DN42 的根证书。请查看[此 Wiki](https://dn42.dev/services/Certificate-Authority)。

Feel free to contact me via email 欢迎通过邮件联系我

dn42 {at) potat0 [dot} cc

## Requirements 要求

- For now, I only accept tunnel connections using WireGuard. My WireGuard AllowedIPs are as follow. 目前，我只接受使用 WireGuard 的隧道连接。我的 WireGuard AllowedIPs 如下。

  ```
  AllowedIPs = 172.20.0.0/14
  AllowedIPs = 10.0.0.0/8
  AllowedIPs = fd00::/8
  AllowedIPs = fe80::/64
  ```
  
- My network only accepts routes that are registered in DN42, and unknown routes (to accomodate newly registered users). 我的网络只允许接收在 DN42 中注册过的路由，以及未知路由（以方便新注册 DN42 的用户）。

- Contact information in the registry must always be up to date and admins must respond when contacted. 在注册处的联系信息必须是有效的，且管理员在需要的时候可以联系得到。

- I don't like to peer with servers in mainland China, but I don't refuse to do it either. If your server is in mainland China, please do let me know. 我不希望与中国大陆服务器进行 Peer，但是也不拒绝。如果你的服务器在中国大陆，请务必告知我。

## Peeeing requests 对等互联请求

In order to set up the peering, I need to know the following information:

为了设置对等互联，我需要知道以下信息：

- The node you want to peer. 你想要对等互联的节点。

- Your WireGuard public key. 你的 WireGuard 公钥。

- The WireGuard endpoint for me to connect. Let me know if it's dynamic or you don't have one. 我要连接到的 WireGuard 公网信息。如果是动态的或者你没有公网地址，记得告诉我。

- Your ASN. 你的 ASN。

- The session(s) to use: IPv6 + IPv4, IPv6 only, or IPv4 only. 要使用的会话：IPv6 + IPv4，仅 IPv6，或仅 IPv4。

- The extra capabilities: Multiprotocol BGP / Extended next hop. 额外的能力：多协议 BGP / 扩展的下一跳。

- The IP address(es): One for each session, and an additional IPv4 if you use MP-BGP without ENH. IP 地址：每个会话只需要一个，如果你用 MP-BGP 且不用 ENH，则同时需要 IPv6 和 IPv4 地址。

E.g.:
```
Node: US-East-1
Public key: LUwqKS6QrCPv510Pwt1eAIiHACYDsbMjrkrbGTJfviU=
Endpoint: us1.dn42.potat0.cc:21816
ASN: 4242421816
Sessions: IPv6 + IPv4
Capabilities: MP-BGP, ENH
IPv6: fe80::1816
IPv4: None
```

## If you are the initiator 如果你是发起人

Set up your side of the peering according to the general and node-specific information first, and then send your information to me (See the beginning of this page for contact information) according to the Peering requests section.

按照通用和节点特定的信息，先将你那边的对等互联设置好，然后按照对等互联请求一节的内容，将你的信息发送给我（联系方式见本页开头）。

I prefer to use MP-BGP and ENH for Peer only over IPv6 Link-Local addresses.

我偏好使用 MP-BGP 和 ENH 来只通过 IPv6 Link-Local 地址进行 Peer。

| General information | 通用信息                    |
|:-------------------:|:--------------------------:|
| ASN                 | 4242421816                 |
| Tunnel type         | WireGuard                  |
| Listen port         | last 5 digits of your ASN  |
| Link-local IPv6     | fe80::1816/64              |
| Multiprotocol BGP   | default: Enabled           |
| Extended next hop   | default: Enabled           |

## Nodes 节点

Read the general information above first!

先看上面的通用信息！

### US-East-1

New York, US, BuyVM 美东 纽约

- WireGuard Public Key 公钥
  
  `LUwqKS6QrCPv510Pwt1eAIiHACYDsbMjrkrbGTJfviU=`

- Connectivity 连接性
  
  IPv4 + IPv6 (1Gbps)

- Endpoint 公网信息

    - IPv4/6:

      `us1.dn42.potat0.cc`

    - IPv4:

      `v4.us1.dn42.potat0.cc`

      `198.98.56.83`

    - IPv6:

      `v6.us1.dn42.potat0.cc`

      `2605:6400:10:ffc:de30:1d96:e61e:43ff`

- DN42

    - `fe80::1816/64`

    - `172.23.246.1/32`

    - `fd2c:1323:4042::1/128`
