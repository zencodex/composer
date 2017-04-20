### 一、如何安装 Composer

#### Linux/Mac系统：

    # 如遇权限不足，可添加 sudo 
    wget https://dl.laravel-china.org/composer.phar -O /usr/local/bin/composer
    chmod a+x /usr/local/bin/composer
 
#### Windows系统：

1. 直接下载 composer.phar，地址：https://dl.laravel-china.org/composer.phar

2. 把下载的 composer.phar 放到 PHP 安装目录

3. 新建 composer.bat, 添加如下内容，并保存：  

```
@php "%~dp0composer.phar" %*
```

#### 查看当前版本：

    composer -V

#### 升级版本：

```
# 升级命令会连接官方服务器，速度很慢
# 建议直接下载我们的 composer.phar 镜像，每天都会更新到最新
composer selfupdate
```

### 二、配置 Composer 镜像

全局配置：

    composer config -g repo.packagist composer https://packagist.laravel-china.org
 
如果仅限当前工程使用镜像，去掉 -g 即可，如下：    
 
    composer config repo.packagist composer https://packagist.laravel-china.org

### 三、遇到问题肿么办？

composer 命令后面加上 -vvv （是3个v），如下：

    composer -vvv create-project laravel/laravel blog
    composer -vvv require psr/log
   
如果自己解决不了，或发现 bug，可以在 @扣丁禅师 的 github 上创建 issue，地址:   
https://github.com/zencodex/composer/issues/new

注意提问时带上 -vvv 的输出，提问要叙述清晰，不要提交无厘头的问题，关于提问的智慧，请看这篇文章：  
https://laravel-china.org/topics/2396/wisdom-of-asking-questions-chinese-version
