# goバージョン
FROM golang:1.22.5-alpine
# アップデートとgitのインストール
RUN apk update && apk add git && apk add bash
# boiler-plateディレクトリの作成
RUN mkdir -p /go/src/github.com/boiler-plate
# ワーキングディレクトリの設定
WORKDIR /go/src/github.com/boiler-plate
# ホストのファイルをコンテナの作業ディレクトリに移行
ADD . /go/src/github.com/boiler-plate
# パッケージのインポート
RUN go install golang.org/x/tools/cmd/goimports@latest
