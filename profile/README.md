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


# 構想だけのTODO
## UnityのUIの上に乗せるUIライブラリ
## Scene管理ライブラリ
## ネットワーク通信ライブラリ
* リアルタイム通信
* NetcodeForGameObject(NGO)の上に乗っける・・・？
  * もしくはトランスポートライブラリのみ他を使ってNetcode周りは自作する・・・？