# 分析内容
データベースよりゲノムデータを取得して、local blastの結果をpythonで分析する

# 分析
## データの取得
aria2を用いてENAからfastqを高速で取得する

今回は以下のHiseqデータを取得する


docker環境にて以下のコマンドでaria2をinstallしてファイルのダウンロード
```bash
# docker containerの起動
docker container run -it --rm -v $(pwd):/app ubuntu

# aria2の取得
apt install aria2 -y

# fileのダウンロード
ftp.sh
```

# biocondaで必要なライブラリーの取得
```docker
conda create -n genome_pipline -y
conda activate genome_pipline
bash library.sh
```

## assembleの実行, roaryによるパンゲノム解析
docker環境で以下のパイプラインの実行
```docker
bash pipline.sh
```

## アクネ菌病原性遺伝子のBLAST
docker環境で以下のコマンドを実行
```docker

```

## BLAST結果の解析と可視化
```docker

```
