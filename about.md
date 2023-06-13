 ---
layout: page
title: About
permalink: /about/
---

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>中英转换</title>
    <script type="text/javascript" src="js/language.js"></script>
    <style>
        .bar{list-style:none; display: flex;padding-top: 30px;}
        .bar li {width: 100px;height: 30px; text-align: center; line-height: 30px; transition: 0.3s;}
        .bar li:hover{background-color: #ccc;}
        .toggle{position: absolute; top: 50px; right: 50px;}
    </style>
</head>
<body>
    <ul class="bar">
        <li id="home">首页</li>
        <li id="recommend">推荐</li>
        <li id="message">消息</li>
        <li id="my">我的</li>
    </ul>
    <button type="button" class="toggle">切换语言</button>
    
    <script>
        var lang_flag = 0;   //lang_flag 作为语言类型的标识，0代表中文，1代表英语
        var toggle = document.getElementsByClassName("toggle")[0];
        toggle.onclick  = function(){
            (lang_flag == 0) ? (lang_flag = 1) : (lang_flag = 0)  //三元运算符
            toggleLan();
        }
        function toggleLan() {
            console.log(home[lang_flag]);
            document.getElementById("home").innerHTML = home[lang_flag]
            document.getElementById("recommend").innerHTML = recommend[lang_flag]
            document.getElementById("message").innerHTML = message[lang_flag]
            document.getElementById("my").innerHTML = my[lang_flag]
        }
    </script>
</body>
</html>
