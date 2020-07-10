# laradoc

# ディレクトリ構成
以下のようにディレクトリを作ってください。
* db
* laradoc※ここcloneしてください。laradoc/laradocじゃないあですよ
* web
    * lara7

## コンテナを立てる
* laradoc$ docker-compose up -d --build workspace postgres php-fpm apache2 pgadmin

## laravelを作る 
* laradoc$ $docker-compose exec workspace bash
* cd html 

### laravelインストール
    * html$ composer global require hirak/prestissimo laravel/installer && composer create-project --prefer-dist laravel/laravel  laravel ./lara7

### パッケージを入れてインストール
    * html$ cd lara7
    * html/lara7$ composer require --dev nunomaduro/larastan
    * html/lara7$ composer require laravel/ui
    * html/lara7$ composer update && composer install

#### Class 'Carbon\Laravel\ServiceProvider' not found

上記のエラがー出たら
* html/lara7$ rm -rf vendor && composer install --no-dev

