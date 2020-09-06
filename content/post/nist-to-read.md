---
author: Naoki Oketani
title: これから読みたいNIST文書
date: 2020-09-06
description: 気になっているNIST文書のリスト
tags:
- security
---

inductor's blogの[これから読みたい論文メモ](https://blog.inductor.me/entry/2020/08/27/105821)に感化されました。
これから読もうと考えているNIST文書を挙げてみます。

## 1. NIST SP 800-190 Application Container Security Guide

https://csrc.nist.gov/publications/detail/sp/800-190/final

コンテナセキュリティを語るうえで欠かせない文書です。一発目は本記事タイトルに沿わず、すでに何度も読んでいます。
コンテナアプリケーションの構成要素を6つに分類し、それぞれにおけるリスク、対策を説明しています。

1. イメージ
2. レジストリ
3. オーケストレーター
4. コンテナ
5. ホスト
6. ハードウェア

つい先日、IPAから翻訳が出ました。英語が苦手な方もどうぞ。

https://www.ipa.go.jp/files/000085279.pdf

## 2. NIST IR-8176 Security Assurance Requirements for Linux Application Container Deployments

https://www.nist.gov/publications/security-assurance-requirements-linux-application-container-deployments

Linux Kernelの機能を利用してコンテナの分離をする方法が説明されていそうです。

- Namespaces
- Cgroups
- Capabilities

## 3. NIST SP 800-204 Security Strategies for Microservices-based Application Systems

https://csrc.nist.gov/publications/detail/sp/800-204/final

コンテナアプリケーションといえば、マイクロサービスです。語弊はあるでしょうが、関連して押さえた方がよさそうと意味で挙げてみました。

## 4. NIST SP 800-207 Zero Trust Architecture

https://csrc.nist.gov/publications/detail/sp/800-207/final

イマドキ流行りのゼロトラストです。オライリー本とSoftware Design 8-10月号の短期連載と併読して理解したいです。

## 5. NIST SP 800-171 Rev. 2 Protecting Controlled Unclassified Information in Nonfederal Systems and Organizations

https://csrc.nist.gov/publications/detail/sp/800-171/rev-2/final

Rev. 1はIPAから翻訳が出ていますが、2020/2/21にRev. 2が出たそうです。

https://www.ipa.go.jp/files/000057365.pdf
