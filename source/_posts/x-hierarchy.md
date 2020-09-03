---
title: X11 Data Structure Hierarchy
date: 2020-09-03 16:49:16
tags: [X11]
---

# X Window System
X Window System是一个基于网络的窗口系统协议，它的一个实现是[Xorg](https://www.x.org/wiki/)。

<!--more-->

# What are data structures in Xorg?
- Display
- Screen
- Depth
- Visual

# How are they organized?
```mermaid
graph TD
    D[Display]
    D --> s0(Screen0)
    D --> s1(Screen1)
    D --> sN(ScreenN)
    subgraph Screen0
    s0 --> d0(Depth0)
    s0 --> d1(Depth1)
    s0 --> d2(Depth2)
    s0 --> d3(Depth3)
    s0 --> dN(DepthN)
    end
    subgraph Depth0
    d0 --> v0(Visual0)
    d0 --> v1(Visual1)
    d0 --> v2(Visual2)
    d0 --> v3(Visual3)
    d0 --> v4(Visual4)
    d0 --> v5(Visual5)
    d0 --> vN(VisualN)
    end
```