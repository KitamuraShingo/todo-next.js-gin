# ベースイメージを指定
FROM node:22-alpine
# コンテナ内の作業ディレクトリを設定
WORKDIR /app

# ホストのpackage.jsonをコンテナの作業ディレクトリにコピー
COPY package.json package-lock.json ./

#ソースコードをコピー
COPY . .

# パッケージをインストール
RUN npm install

# ポート3000番を開放
EXPOSE 3000

# コンテナを起動する際に実行されるコマンド
CMD ["npm", "run", "dev"]
