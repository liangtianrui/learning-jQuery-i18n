# learning-jQuery i18n

## jquery i18n的学习之旅

### 为何学习JQuery i18n

现在随着业务的需求，需要将网站语言支持多语言,这个着实给不管是前台还是后台都增加了不小的挑战，因为之前做的时候根本没有考虑多语言的问题，导致很多页面写的不是很灵活，样式写的比较死 ,所以,你想变得灵活一些,所以用到JQuery i18n

### JQuery i18n简介

> 在介绍 jQuery.i18n 之前，我们先来看一下什么是国际化。国际化英文单词为：Internationalization，又称 i18n，“i”为单词的第一个字母，“18”为“i”和“n”之间单词的个数，而“n”代表这个单词的最后一个字母。在计算机领域，国际化是指设计能够适应各种区域和语言环境的软件的过程。

> jQuery.i18n 是一款轻量级的 jQuery 国际化插件。与 Java 里的资源文件类似，jQuery.i18n 文件对 JavaScript 进行国际化。jQuery.i18n 插件根据用户指定的（或浏览器提供的 ）语言和国家编码（符合 [ISO-639](https://baike.baidu.com/item/iso%20639) 和 [ISO-3166](https://baike.baidu.com/item/ISO%203166-1/5269555?fr=aladdin) 标准）来解析对应的文件。

> 利用资源文件实现国际化是一种比较流行的方式，例如 Android 应用就可以采用以语言和国家编码命名的资源文件来实现国际化

### jQuery.i18n 特点

1. 支持根据设置默认语言
2. 支持切换语言
3. 支持使用json文件存储翻译内容
4. 可以根据用户自定义的不同语言版本的 json 文件，按需渲染网页上的语言，实现国际化。

### 创建文件

#### 1.创建 learning-jQuery-i18n

![webStrom](https://github.com/liangtianrui/learning-jQuery-i18n/blob/master/image/webStrom.png?raw=true)

![create](https://github.com/liangtianrui/learning-jQuery-i18n/blob/master/image/create.png?raw=true)

#### 2.创建文件夹examples

![examples](https://github.com/liangtianrui/learning-jQuery-i18n/blob/master/image/examples.png?raw=true)



#### 3.创建index.html文件

![indexHtml](https://github.com/liangtianrui/learning-jQuery-i18n/blob/master/image/indexhtml.png?raw=true)

#### 4.index.html页面代码

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>jQuery i18n Plugin</title>
    <style type="text/css">
        body {
            font-size: 30px;
            text-align: center;
        }
        input {
            font-size: 30px;
        }
        p {
            font-size: 17px;
        }
    </style>
</head>
<body>
<h1>
    点击👇就会有惊喜
</h1>

<div id='example1'>Example 1</div>
<div id='example2'>Example 2</div>
<div id='example3'>Example 3</div>
<div id='example4'>Example 4</div>
<div id='example5'>Example 5</div>
<input type='button' id='btn' value='Internationalize!' />

</body>
</html>
```

##### 5.引入jQuery

![script](https://github.com/liangtianrui/learning-jQuery-i18n/blob/master/image/script.png?raw=true)

```
<script src="../jquery-1.4.2.js"></script>
<script src="../jquery.i18n.min.js"></script>

```

![src](https://github.com/liangtianrui/learning-jQuery-i18n/blob/master/image/src.png?raw=true)

#### 6.script 文件

```
<script  type="text/javascript">
    $(document).ready(function(){
        i18n_dict = {
            "Example 1"  : '案例1',
            "Example 2"  : "案例2",
            "Example 3"  : "案例3",
            "Example 4"  : "案例4",
            "Example 5"  : "案例5",

        };

        $.i18n.load(i18n_dict);

        $('#btn').click( function(event) {
            $('#example1')._t('Example 1');
            $('#example2')._t('Example 2');
            $('#example3')._t('Example 3');
            $('#example4')._t('Example 4');
            $('#example5')._t('Example 5');
        });
    });
</script>
```

##### 7.i18n_dict 相当于字典

```
 i18n_dict = {
            "Example 1"  : '案例1',
            "Example 2"  : "案例2",
            "Example 3"  : "案例3",
            "Example 4"  : "案例4",
            "Example 5"  : "案例5",
        };
```

##### 8.运行i18n

```
$.i18n.load(i18n_dict);
```

##### 9.点击事件

```
 $('#btn').click( function(event) {
            $('#example1')._t('Example 1');
            $('#example2')._t('Example 2');
            $('#example3')._t('Example 3');
            $('#example4')._t('Example 4');
            $('#example5')._t('Example 5');
        });
```

##### 10. _t 含义



