---
layout: blog
title: 全部文章
description: Every great website starts with a great homepage. The homepage tells your viewers what your site is all about and gives your viewers a place to come back to.
sitemap:
    priority: 1.0
    lastmod: 2017-11-02
    changefreq: weekly
---


    <title>网站以迁移。</title>
    <script type="text/javascript">
        // 在页面加载完成后执行
        window.onload = function() {
            // 弹出提示框告知用户网站已迁移
            var confirmStatus = confirm("我的博客已迁移至新地址，现在将为您跳转...");
            if(confirmStatus) {
                // 用户点击“确定”后进行跳转
                window.location.href = "http://www.shirleytan.top"; // 请将此URL替换为实际的新网站URL
            } else {
                // 用户点击“取消”，可以选择是否也进行跳转或做其他处理
                window.location.href = "http://www.shirleytan.top"; // 重复设置以确保最终总是跳转，可按需修改逻辑
            }
        };
    </script>
