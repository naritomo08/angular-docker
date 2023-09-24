# angular-docker

angular環境を立ち上げることができます。

## 参考URL

[Angular環境構築手順（Docker上に構築する）](https://shiraberu.tech/2021/11/24/angular-setup-on-docker/)

## 事前準備

mac+DockerCompose+vscode+gitでの環境を構築してること。

## 開発環境構築方法(Angular)

### docker構成ソース入手

以下のコマンドで入手する。

```bash
git clone https://github.com/naritomo08/angular-docker.git
cd angular-docker
```

### コンテナ立ち上げ

```bash
docker-compose build
docker-compose run --rm sample-angular sh -c "npm install"
→上記コマンドは初回のみ
docker-compose up -d
```

### サイト確認

以下のURLにアクセスし、Angularトップ画面が出てくること。

```bash
http://localhost:4200/
```

### コンテナログイン

```bash
docker-compose exec sample-angular bash
```

## 開発環境操作

### 開発環境コンテナ起動/設定再読み込み

```bash
docker-compose up -d
```

### 開発環境コンテナ停止

```bash
docker-compose stop
```

### 開発環境コンテナ破棄

```bash
docker-compose down
```