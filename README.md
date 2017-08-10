# learning-jQuery i18n

## jquery i18n的学习之旅

### 为何学习JQuery i18n

现在随着业务的需求，需要将网站语言支持多语言,这个着实给不管是前台还是后台都增加了不小的挑战，因为之前做的时候根本没有考虑多语言的问题，导致很多页面写的不是很灵活，样式写的比较死 ,所以,你想变得灵活一些,所以用到JQuery i18n

### JQuery i18n简介

> 在介绍 jQuery.i18n 之前，我们先来看一下什么是国际化。国际化英文单词为：Internationalization，又称 i18n，“i”为单词的第一个字母，“18”为“i”和“n”之间单词的个数，而“n”代表这个单词的最后一个字母。在计算机领域，国际化是指设计能够适应各种区域和语言环境的软件的过程。

> jQuery.i18n 是一款轻量级的 jQuery 国际化插件。与 Java 里的资源文件类似，jQuery.i18n 文件对 JavaScript 进行国际化。jQuery.i18n 插件根据用户指定的（或浏览器提供的 ）语言和国家编码（符合 [ISO-639](https://baike.baidu.com/item/iso%20639) 和 [ISO-3166](https://baike.baidu.com/item/ISO%203166-1/5269555?fr=aladdin) 标准）来解析对应的文件。



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
<script src="../jquery-1.4.2.js"></script>
<script src="../jquery.i18n.min.js"></script>
<body>
<h1>
    点击👇就会有惊喜
</h1>
<div id='test1'>Test  One</div>
<div id='test2'>Test2  Two</div>
<div id='test3'>Test3  Three</div>
<div id='test4'>Test4  Four</div>
<div id='test5'>Test5  Five</div>
<input type='button' id='btn' value='Internationalize!'/>

</body>
```



##### 5.引入jQuery

![script](https://github.com/liangtianrui/learning-jQuery-i18n/blob/master/image/script.png?raw=true)

```
<script src="../jquery-1.4.2.js"></script>
<script src="../jquery.i18n.min.js"></script>
```

![src](https://github.com/liangtianrui/learning-jQuery-i18n/blob/master/image/src.png?raw=true)



##### 6. i18n_dict 相当于字典

```
 i18n_dict = {
            'test1': '测试  1',
            'test2': '测试  2',
            'test3': '测试  3',
            'test4': '测试  4',
            'test5': '测试  5'
        }
```



##### 7.运行i18n

```
$.i18n.load(i18n_dict);     $.i18n.load() 参数1 : 运行将要转换的代码
```



##### 8.点击事件

```
         $('#btn').click(function () {
            $('#test1')._t('test1');
            $('#test2')._t('test2');
            $('#test3')._t('test3');
            $('#test4')._t('test4');
            $('#test5')._t('test5');
        })
```



##### 9. _t ()含义

​     _t()参数1 : 将要转换的参数名 



##### 10.scritpt完整代码

```	
<script>

    $(document).ready(function () {
        i18n_dict = {
            'test1': '测试  1',
            'test2': '测试  2',
            'test3': '测试  3',
            'test4': '测试  4',
            'test5': '测试  5'
        }

        $.i18n.load(i18n_dict);
        
        $('#btn').click(function () {
            $('#test1')._t('test1');
            $('#test2')._t('test2');
            $('#test3')._t('test3');
            $('#test4')._t('test4');
            $('#test5')._t('test5');
        })
    })
</script>
```





### *注 : 以上代码只是简单的实现原理  ,  只代表个人立场,如在使用上述代码时出现任何情况,概不负责。  

