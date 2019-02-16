---
title: scrapy语法
tags:
  - scrapy
  - xpath
  - css
date: 2018-03-03 11:37:26
top:
---

## xpath语法
表达式 | 说明 
---- | ---
article | 选取所有article元素的所有子节点
/article | 选取根元素article
article/a | 选取所有属于article的子元素的a元素
//div | 选取所有div子元素
article//div | 选取所有属于article元素的后代div元素
//@class | 选取所有名为class的属性

## xpath语法-谓语
表达式 | 说明 
---- | ---
/article/div[1] | 选取属于article子元素的第一个div元素
/article/div[last()] | 选取属于article子元素的最后一个div元素
/article/div[last()]  | 选取属于article子元素的倒数第二个div元素
//div[@lang] | 选取所有拥有lang属性的div元素
//div[@lang='eng'] | 选取所有lang属性为eng的div元素

## xpath语法-其他
表达式 | 说明 
---- | ---
/div/* | 选取属于div元素的所有子节点
//* | 选取所有元素
//div[@*]  | 选取所有带属性的div元素
//div/a \| //div/p | 选取所有div元素的a和p元素
//span \| //ul | 选取文档中的span和ul元素

## css选择器
表达式 | 说明 
---- | ---
* | 选择所有节点
\#contriner | 选择id为contriner的节点
.container | 选取所有class包含container的节点
li a | 选取所有li下的所有a节点
ul + p | 选择ul后面的第一个p元素
div#container > ul | 选取id为container的div的第一个ul子元素

## css选择器进阶
表达式 | 说明 
---- | ---
ul ~ p | 选取与ul相邻的所有p元素
a[title] | 选取所有有title属性的a元素
a[href="xxx"] | 选取所有href属性为xxx值的a元素 
a[href*="xxx"] | 选取所有href属性包含xxx的a元素 
a[href^="xxx"] | 选择所有href属性以xxx开头的a元素
a[href$=".jpg"] | 选取所有href属性以.jpg结尾的a元素
input[type=radio]:checked | 选择选中的radio的元素
div:not(#container) | 选取所有id非container的div属性
li:nth-child(3) | 选取第三个li元素
tr:nth-child(2n) | 第偶数个tr
