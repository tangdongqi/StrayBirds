---
layout: post
title: Firewall Stateful or Stateless
category: tcp
comments: true
---
A firewall can be described as being either Stateful, or Stateless.

STATELESS

Stateless firewalls watch network traffic, and restrict or block packets based on source and destination addresses or other static values. They are not 'aware' of traffic patterns or data flows. A stateless firewall uses simple rule-sets that do not account for the possibility that a packet might be received by the firewall 'pretending' to be something you asked for.

STATEFUL

Stateful firewalls can watch traffic streams from end to end. They are are aware of communication paths and can implement various IP Security (IPsec) functions such as tunnels and encryption. In technical terms, this means that stateful firewalls can tell what stage a TCP connection is in (open, open sent, synchronized, synchronization acknowledge or established), it can tell if the MTU has changed, whether packets have fragmented etc.

Neither is really superior and there are good arguments for both types of firewalls. Stateless firewalls are typically faster and perform better under heavier traffic loads. Stateful firewalls are better at identifying unauthorized and forged communications.

```
防火墙可以被描述为是有状态，无状态的。

无状态

无状态防火墙收看网络通信，以及限制或基于源地址和目的地址或其他静态值阻止数据包。他们不是流量模式或数据流“识别”。无状态防火墙使用简单的规则集不占，一个数据包可能被防火墙收到'假装'要的东西你要的可能性。

STATEFUL

有状态防火墙可以从头到尾观看交通流。它们都知道的通信路径，并且可以实现各种IP安全（IPsec）的功能，例如隧道和加密。在技​​术方面，这意味着状态防火墙能告诉什么阶段TCP连接是(open, open sent, synchronized, synchronization acknowledge or established)，它可以告诉如果MTU发生了变化，包是否有碎片等

也不是真的优越，有两种类型的防火墙很好的理由。无状态防火墙通常更快，更重的交通负荷下有更好的表现。有状态防火墙查明非法结下通信更好。
