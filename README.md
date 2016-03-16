# Spring Intern 2016 API sapmles

## ローカル環境で立ち上げる

### 準備

[Docker Toolbox](https://www.docker.com/products/docker-toolbox)を用いる。

インストーラーを使って以下の手順を踏むか、

https://docs.docker.com/mac/step_one/

もしくは、Homebrew caskを使って以下のようにセットアップする。

```
$ brew cask dockertoolbox
$ docker-machine create --driver virtualbox default
$ eval $(docker-machine env default)
```

```
$ docker -v
Docker version 1.10.1, build 9e83765
```

のように出力されれば成功！

### 立ち上げ

まず、このリポジトリをCloneする。

```
$ git clone git@github.com:wantedly/spring-intern-2016-api-samples.git
$ cd spring-intern-2016-api-samples
```

このディレクトリ以下で

```
$ docker-compose up
```

した後、

```
$ open http://`docker-machine ip default`:8080
```

でローカルのdocker-machine上で動いているサーバーにつなぐことが出来る。


デフォルトで、Pythonのサンプルが立ち上がるようになっている。
Rubyのサンプルもあるのでそれを立ち上げたい場合、`docker-compose.yml`の`build`の部分を`python`から`ruby`に書き換える。
これは言語を指定しているわけではなく、ディレクトリを指定しているだけなので誤解しないように。

```
web:
  build: ruby
  ports:
    - "8080"
```
