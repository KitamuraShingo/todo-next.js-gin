# ベースイメージを指定
FROM golang:latest
# コンテナ内の作業ディレクトリを設定
WORKDIR /app

#ローカルファイルをコンテナにコピー
COPY . .

# go.modとgo.sumをコピーして依存関係を解決
RUN go mod download

# ビルド
RUN go build -o main .

EXPOSE 8080

CMD ["go", "run", "main.go"]
