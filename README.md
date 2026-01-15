# Deep Workspace

このプロジェクトは．NVIDIA GPUを有するサーバ上で深層学習，大規模言語モデル関連の研究開発を行うためのPython開発環境をセットアップするためのリポジトリです．
個人PC（のVisual Studio Code）からSSHでGPUサーバに接続し，GPUサーバ上で稼働している仮想環境で開発を行うことを想定しています．

リポジトリを活用するためには，個人PC，GPUサーバに以下のソフトウェアがインストールされている必要があります．

個人PC
- Visual Studio Code
- Remote - SSH（Visual Studio Codeの拡張）
- Dev Containers（Visual Studio Codeの拡張）

GPUサーバ
- NVIDIAドライバ
- Docker
- NVIDIA Container Toolkit

※ やまもとの研究室のサーバには，上記ソフトウェアはインストール済みです．
サーバの接続情報を用意すれば，すぐに開発環境をセットアップできます．
