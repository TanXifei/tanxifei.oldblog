---
layout: post
title:  "上海三菱电梯通配化装潢丨标配 PPT资源下载"
date:   2025-01-20
excerpt: "你是不是要下载？往下看"
image: "https://pic2.ziyuan.wang/user/tanxifei/2024/11/29_eee5fe351e766.jpg"
---

# 请务必仔细阅读说明

## 工程文件夹整体打包 不提供使用方法 请自行研究

## 内显“司机” “检修”过于复杂 能力限制没有制作

### 制作外显/内显界面时 建议复制全显进行修改

### 导出外显/内显图片时 请将背景替换为黑色 便于嵌入

## 请确认以下信息:

### 阅读下面四行文字后 点击每行最后一个字，按顺序正确点击后 会出现下载按钮
<!-- 四个复选框 -->
<label><input type="checkbox" name="option" onclick="handleCheckboxClick(this)"> 我要下载的是<a href="https://www.bilibili.com/video/BV1W4cHeZErc" target="_blank">这个视频中</a>PPT的资源文件</label><br>
<label><input type="checkbox" name="option" onclick="handleCheckboxClick(this)"> 我知道这是整个工程文件打包</label><br>
<label><input type="checkbox" name="option" onclick="handleCheckboxClick(this)"> 我明白视频用的“组合 合并.pptx”里面的显示屏由其他PPT导出</label><br>
<label><input type="checkbox" name="option" onclick="handleCheckboxClick(this)"> 我知道有部分元素缺失</label><br>

<!-- 跳转按钮，初始状态下是隐藏的 -->
<button id="submitButton" style="display:none;" onclick="location.href='https://dl.tanxifei.top/%E6%A8%A1%E6%8B%9F%E7%94%B5%E6%A2%AF%E7%B4%A0%E6%9D%90/%E4%B8%8A%E6%B5%B7%E4%B8%89%E8%8F%B1%E9%80%9A%E9%85%8D%E5%8C%96%E4%B8%A8%E6%A0%87%E9%85%8D%E4%B8%A8ND10+GD10+A11.zip';">我要下载！</button>

<script type="text/javascript">
function handleCheckboxClick(checkbox) {
    alert('该行' + (checkbox.checked ? '已确认' : '未确认'));
    checkAllBoxes();
}

function checkAllBoxes() {
    var checkboxes = document.querySelectorAll('input[name="option"]');
    var button = document.getElementById('submitButton');
    var allChecked = true;
    for (var i = 0; i < checkboxes.length; i++) {
        if (!checkboxes[i].checked) {
            allChecked = false;
            break;
        }
    }
    button.style.display = allChecked ? 'block' : 'none';
}

window.onload = function() {
    checkAllBoxes();
}
</script>
