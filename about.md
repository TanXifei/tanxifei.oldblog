---
layout: page
title: 本页面已迁移到新站点
description: 
sitemap:
    priority: 0.7
    lastmod: 2038-12-31
    changefreq: weekly
---
<head>
    <title>网站以迁移。</title>
    <script type="text/javascript">
        // 在页面加载完成后执行
        window.onload = function() {
            // 弹出提示框告知用户网站已迁移
            var confirmStatus = confirm("我的博客已迁移至新地址，现在将为您跳转到新的“关于”页...");
            if(confirmStatus) {
                // 用户点击“确定”后进行跳转
                window.location.href = "http://www.shirleytan.top/start-page.html"; // 请将此URL替换为实际的新网站URL
            } else {
                // 用户点击“取消”，可以选择是否也进行跳转或做其他处理
                window.location.href = "http://www.shirleytan.top/start-page.html"; // 重复设置以确保最终总是跳转，可按需修改逻辑
            }
        };
    </script>
</head>
<body>
    <h1>如果未跳转，请点击下面的链接</h1>
    <a href="http://www.shirleytan.top/start-page.html">前往新页面</a>
</body>
