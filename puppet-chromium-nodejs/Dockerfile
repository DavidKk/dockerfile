# 基础镜像
# glibc 必须大于 2.33
FROM debian:bookworm-slim AS builder

# 更新并初始化
RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y curl tar xz-utils python3 make g++ git chromium

# # 安装 NodeJS 与 NPM
RUN apt-get install -y nodejs npm

# 安装 NodeJS 版本管理器
RUN npm i -g n

# 安装最新 Nodejs
RUN n latest

# 升级 NPM
RUN npm i -g npm@latest

# 开启 corepack
RUN corepack enable
