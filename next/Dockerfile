FROM node:19.4.0
WORKDIR /app
# イメージのベースとなるDockerイメージを指定
FROM node:latest

# ワーキングディレクトリを設定
WORKDIR /app

# ユーザーを切り替える
USER root

# 依存関係をインストール
COPY package*.json ./
RUN npm install

# ソースコードをコピー
COPY . .

# ポートを公開
EXPOSE 3000

# コンテナが起動した時に実行されるコマンドを設定
CMD ["npm", "start"]