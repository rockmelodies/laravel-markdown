# laravel-markdown

一个解析Markdown为html的laravel组件,兼容html和markdown

# 官网介绍

<a href="https://larashuo.com">larashuo视频教程网</a>

# 站长个人微信

<img src="https://larashuo.com/front/laracasts/images/larashuo-kf.png">

# 安装
````
composer require laramall/laravel-markdown

````

# 配置

````
php artisan vendor:publish

配置文件 config/markdown.php

'driver' => 'github'

driver可能的值

github
github解析模式

all     
traditional markdown and parse full text

extra   
use markdown extra

inline  
parse only inline elements (useful for one-line descriptions)

````

# 系统要求

````
php >= 7.0

laravel >= 5.1

````

# 使用

<img src="https://ecsvip.com/201712/markdown-cover.png">

````
使用github模式
Markdown::html('# 测试标题')
转化后的文字是
<h1>测试标题</h1>\n



使用all模式
Markdown::driver('all')->html('# 测试标题');
转化后的文字是
<h1>测试标题</h1>\n


使用extra模式
Markdown::driver('extra')->html('#{.red-text} 测试标题');
转化为
<h1 class="red-text"> 测试标题</h1>\n


使用inline模式
Markdown::driver('inline')->html('# 测试标题');
转化为
#测试标题

````
