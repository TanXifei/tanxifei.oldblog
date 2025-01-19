---
layout: page
title: 什么，这叫关于？（
description: 
sitemap:
    priority: 0.7
    lastmod: 2038-12-31
    changefreq: weekly
---
<!DOCTYPE html>
<html>
<head>
<title>请确认以下信息</title>
<script type="text/javascript">
function checkAllBoxes() {
    // 获取所有的input元素，其中type为checkbox
    var checkboxes = document.getElementsByName('option');
    var button = document.getElementById('submitButton');
    var allChecked = true;

    // 检查每个复选框是否被选中
    for (var i = 0; i < checkboxes.length; i++) {
        if (!checkboxes[i].checked) {
            allChecked = false;
            break;
        }
    }

    // 根据复选框的状态显示或隐藏按钮
    button.style.display = allChecked ? 'block' : 'none';
}

// 当页面加载完成时，先检查一次复选框状态
window.onload = function() {
    checkAllBoxes();
}
</script>
</head>
<body>

<h3>Select all checkboxes to reveal the button:</h3>

<!-- 四个复选框 -->
<input type="checkbox" name="option" onclick="checkAllBoxes()">我要下载的是“上海三菱电梯”PPT的资源文件<br>
<input type="checkbox" name="option" onclick="checkAllBoxes()">我知道这是整个工程文件打包<br>
<input type="checkbox" name="option" onclick="checkAllBoxes()">我明白视频用的是“组合 合并.pptx 里面的显示屏由其他PPT导出<br>
<input type="checkbox" name="option" onclick="checkAllBoxes()">转载请标明出处<br>

<!-- 跳转按钮，初始状态下是隐藏的 -->
<button id="submitButton" style="display:none;" onclick="location.href='http://example.com';">我要下载！</button>

</body>
</html>
