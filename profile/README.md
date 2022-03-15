<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**

- [IfritLibrary](#ifritlibrary)
  - [ExeToDll](#exetodll)
    - [内容](#%E5%86%85%E5%AE%B9)
  - [DebugLogger](#debuglogger)
    - [Dependency](#dependency)
    - [内容](#%E5%86%85%E5%AE%B9-1)
  - [TCPConnecter](#tcpconnecter)
    - [Dependency](#dependency-1)
    - [内容](#%E5%86%85%E5%AE%B9-2)
  - [MessageEditor](#messageeditor)
    - [Dependency](#dependency-2)
    - [内容](#%E5%86%85%E5%AE%B9-3)
  - [DataSheet](#datasheet)
    - [内容](#%E5%86%85%E5%AE%B9-4)
  - [SoundEventLink](#soundeventlink)
    - [Dependency](#dependency-3)
    - [内容](#%E5%86%85%E5%AE%B9-5)
  - [NetworkLibrary](#networklibrary)
    - [内容](#%E5%86%85%E5%AE%B9-6)
- [構想だけのTODO](#%E6%A7%8B%E6%83%B3%E3%81%A0%E3%81%91%E3%81%AEtodo)
  - [UnityのUIの上に乗せるUIライブラリ](#unity%E3%81%AEui%E3%81%AE%E4%B8%8A%E3%81%AB%E4%B9%97%E3%81%9B%E3%82%8Bui%E3%83%A9%E3%82%A4%E3%83%96%E3%83%A9%E3%83%AA)
  - [Scene管理ライブラリ](#scene%E7%AE%A1%E7%90%86%E3%83%A9%E3%82%A4%E3%83%96%E3%83%A9%E3%83%AA)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# IfritLibrary

## ExeToDll
### 内容
* フォルダーをDLLとして埋め込むことでUnity内でのサードパーティーアプリの実行を簡単にする

## DebugLogger
### Dependency
* ExeToDll
### 内容
* デバッグログを集約する。
* UnityEditor外のサードパーティソフトで作成することにより柔軟な、様々な状況でロギングを出来る
* TCP/IP によりやり取りをしてDebugLogger側でデータ加工を行えるため処理負荷をランタイムから引き離すことが出来る

## TCPConnecter
### Dependency
* ExeToDll
### 内容
* サードパーティアプリとUnityのやり取りを簡易にする
* TCP/IPを使った通信をラッピングしている

## MessageEditor
### Dependency
* ExeToDll
* TCPConnecter
### 内容
* ゲーム内のテキスト全般を扱える
* 文字送り速度、各種タグ、ローカライズが出来る
* TCPConnecterを利用したホットリロード対応

## DataSheet
### 内容
* ゲーム内で使うデータを管理する
* json形式でデータの形式を管理、ScriptableObjectで実際のゲーム内で使えるデータの作成をサポート

## SoundEventLink
### Dependency
* DataSheet
### 内容
* ScriptableObjectSheetMasterMemoryの上に載せていたものをDataSheetに移行

## NetworkLibrary
### 内容
* 検証段階
* UnityTransformの上に乗っけて超多人数がアクセス出来るようにする検証
* 目標は狭い空間に100人、広いワールドで1000人

# 構想だけのTODO
## UnityのUIの上に乗せるUIライブラリ
## Scene管理ライブラリ
