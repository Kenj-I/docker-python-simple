# Docker python script

## About
pythonのスクリプトを実行する用のシンプルなDocker環境

## Usage

docker-compose.yml.orgをコピーして使用
scriptはsrcの中

本番ではこんな感じで実行

例

```
docker-compose run --rm python3 /bin/bash -c "pipenv install --system --ignore-pipfile --deploy && pipenv run app"
```