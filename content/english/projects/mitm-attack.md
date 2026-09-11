---
title: "Man-in-the-Middle Attack"
meta_title: ""
description: "Social engineering and a better understanding of man-in-the-middle attacks."
summary: "A Raspberry Pi running Kali Linux and Wi-Fi Pumpkin, used to show how open public Wi-Fi exposes unencrypted traffic."
date: 2019-12-02T18:07:16+06:00
image: "/images/portfolio/MITM/pie_adapter.jpg"
categories: ["Security"]
author: "Angelo Pana"
tags: ["Kali Linux", "Raspberry Pi", "Wi-Fi Pumpkin"]
draft: false
---

#### Challenge

To better understand how connecting to an open Wi-Fi network in public areas, such as airports or coffee shops, can affect your security and privacy.

#### Solution

To simulate this problem, I introduced a Raspberry Pi with a USB-attached Wi-Fi adapter running Kali Linux to broadcast an open Wi-Fi network in a public area.

![Wi-Fi Pumpkin](https://raw.githubusercontent.com/P0cL4bs/WiFi-Pumpkin/master/docs/screenshot.png)

By using an application called Wi-Fi Pumpkin, I was able to view images and sensitive data. However, only unsecured HTTP websites were viewable; the simulated man-in-the-middle attack was unsuccessful against any request to an HTTPS website.
