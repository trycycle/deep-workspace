# ベースイメージとしてNVIDIAの公式CUDAイメージを使用
FROM nvidia/cuda:13.0.2-cudnn-devel-ubuntu24.04

# 環境変数の設定
ENV TZ=Asia/Tokyo
ENV DEBIAN_FRONTEND=noninteractive
ENV LANG=ja_JP.UTF-8
ENV PIP_BREAK_SYSTEM_PACKAGES=1

# 必要なパッケージのインストールと日本語環境の設定
RUN apt-get update && \
    apt-get install -y \
    build-essential \
    python3 \
    python3-pip \
    python3-dev \
    git \
    locales \
    && apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# 日本語ロケールの設定
RUN locale-gen ja_JP.UTF-8
RUN update-locale LANG=ja_JP.UTF-8

# python3 -> pythonへのシンボリックリンク作成
RUN ln -s /usr/bin/python3 /usr/bin/python

# requirements.txtをコンテナにコピー
# requirements.txtは、Dockerfileと同じディレクトリに配置
COPY requirements.txt /tmp/requirements.txt

# requirements.txt を使ってライブラリをインストール
RUN pip install --no-cache-dir -r /tmp/requirements.txt

# 作業ディレクトリの作成
WORKDIR /workspace
