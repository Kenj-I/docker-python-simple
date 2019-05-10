FROM python:3-slim

# set locale
# サーバーの言語は英語にして日本語入力をできるようにする
RUN apt-get clean && apt-get update && apt-get install -y locales locales-all
RUN locale-gen en_US.UTF-8
ENV LANG ja_JP.UTF-8
ENV LANGUAGE en_US:en
ENV LC_ALL en_US.UTF-8

# timezoneの設定
ENV TZ JST-9

# vim
RUN apt-get install -y vim

# pip & setuptools アップデート
RUN pip install --upgrade pip
RUN pip install --upgrade setuptools

# pipenv
RUN pip install pipenv
# pipenvのパッケージをプロジェクト直下に置く
ENV PIPENV_VENV_IN_PROJECT=1