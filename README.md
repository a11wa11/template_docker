# template_docker

## 概要

dockerで使用するコマンドやDockerfileのテンプレートを用意します

## 使用例

```sh
# 基本ビルドコマンド
docker build -t 名付けたいイメージ名 .(Dockerfileのあるパス)

# Dockerfileを指定してbuild
docker build -f Dockerfile_demo(Dockerfile以外の名前の場合) .(Dockerfileのあるパス)
# Dockerfileを指定し、引数を指定してbuild
docker build --build-arg PLATFORM=arm64 -f Dockerfile_demo(Dockerfile以外の名前の場合) .(Dockerfileのあるパス)
```
