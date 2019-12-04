---
layout:     post
title:      Selenium_元素定位
subtitle:   Selenium 元素定位
date:       2019-8-06
author:     youyr
header-img: img/index1.jpg
catalog: true
tags:
    - selenium
---

<p style="font-size:20px;color:green">&nbsp;&nbsp;&nbsp;&nbsp;通常来说，我们如果想要操作一个元素，那首先就得找到这个元素的位置，那么如何找到这些元素？</p>
<span>webDriver提供了八种定位元素的方法，在python中，所对应的方法如下：</span>

<span style="color:green;font-size:20px">1、Id定位</span>
 <p>&nbsp;&nbsp;&nbsp;&nbsp;学过css的应该知道，如果想要为html元素设置样式，一般需要在元素中设置id和class选择器。一般id选择器用#号来定义，id属性一般是唯一的，有点类似于我们的身份证号。所以可以根据id属性来查找到对应的元素。例如，查找百度页面“百度一下”这个按钮，用法如下：</p>
 <p>find_element_by_id(“su”)</p>
 <p>find_element_by_id()方法通过id属性来定位元素</p>

<span style="color:green;font-size:20px">2、class定位</span>
<p>&nbsp;&nbsp;&nbsp;&nbsp;class是用来指定元素的类名，用法类似于id，可以通过class属性定位“百度一下这个按钮，用法如下：</p>
<p>find_element_class_name(“bg s_btn”)</p>
<p>find_element_class_name()方法通过class属性来定位元素</p>

<span style="color:green;font-size:20px">3、name定位</span>
<p>&nbsp;&nbsp;&nbsp;&nbsp;name在html中是用来指定元素的名称的，有点类似于人名，而且name属性和人名一样是可以重复的。可以通过name属性来定位百度搜索框，用法如下：</p>
<p>find_element_by_name(“wd”)</p>
<p>find_element_by_name()方法通过name属性来定位元素，如果元素中没有name属性，那么不可以用name来定位。</p>

<span style="color:green;font-size:20px">4、tag定位 </span>
<p>&nbsp;&nbsp;&nbsp;&nbsp;tag是标签的意思，它代表前端的标签，比如input,li,a,img等标签。但是一般一个页面中含有大量相同的标签，所以用tag来定位到元素的概率是极低的，一般不推荐用。用法如下：</p>
<p>find_element_by_tag_name(“a”)</p>
<p>find_element_by_tag_name()方法通过元素的tag name(标签名)来定位</p>

<span style="color:green;font-size:20px">5、link定位</span>
<p>&nbsp;&nbsp;&nbsp;&nbsp;link是专门用来定位文本链接的。比如下面这种链接</p>
<p>(a href="http://news.baidu.com" target="_blank" class="mnav">新闻</a>)用法如下：</p>
<p>find_element_by_link_text(“新闻”)</p>
<p>find_element_by_link_text()方法通过链接标签之间的文本来定位元素</p>

<span style="color:green;font-size:20px">6、partail link定位</span>
<p>这种定位是对link的一个补充，用来定位长的文本链接的，所以就不解释了
用法如下：</p>
<p>find_element_by_partail_link_text()</p>
<span style="color:green;font-size:20px">7、xpath定位</span>
<p>&nbsp;&nbsp;&nbsp;&nbsp;XPath 是一门在 XML 文档中查找信息的语言。使用路径表达式来选取 XML 文档中的节点或者节点集。xpath可以直接在浏览器上复制路径，也可以自己写，自己写的话安装一下浏览器插件，chrome的插件是XPath Helper，其他浏览器的自行搜索，另外Xpath的学习建议去搜索一下网上的教程，特别详细。
用法如下：</p>
<p>find_element_by_xpath(//*[@id="kw"])（里面写xpath的路径表达式）</p>

<span style="color:green;font-size:20px">8、css定位</span>
<p>find_element_by_css_selector()方法用于css语言定位元素</p>

<p style="color:green">1)通过class属性定位</p>
<p>find_element_by_css_selector(“.s_ipt”)</p>
<p style="color:green">2)通过id属性定位</p>
<p>find_element_by_css_selector(“#su”)</p>
<p style="color:green">3)通过标签名定位</p>
<p>find_element_by_css_selector(“input”)</p>
<p style="color:green">4)通过父子关系定位</p>
<p>find_element_by_css_selector(“ul>li”)</p>
<p style="color:green">5)通过属性定位</p>
<p>find_element_by_css_selector(“[name=’kw’]”)</p>
<p style="color:green">6)组合定位</p>
<p>find_element_by_css_selector(“div.site-heading>span.subheading”)</p>
<p>（class名为site-heading的div下面的class名为subheading的span标签）</p>
