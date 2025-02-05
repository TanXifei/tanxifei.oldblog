---
layout: post
title:  "测3"
date:   2025-01-20
excerpt: "你是不是要下载？往下看"
image: "https://pic2.ziyuan.wang/user/tanxifei/2024/11/29_eee5fe351e766.jpg"
---

# 请务必仔细阅读说明

## 工程文件夹整体打包 不提供使用方法 请自行研究

## 内显“司机” “检修”过于复杂 能力限制没有制作

### 制作外显/内显界面时 建议复制全显进行修改

### 导出外显/内显图片时 请将背景替换为黑色 便于嵌入
<!-- 下载PPT资源文件 -->

请确认以下信息:

<!-- 四个复选框 -->
<div id="confirmation">
    <label class="checkbox-label">
        <input type="checkbox" name="option" onclick="handleCheckboxClick(this)">
        我要下载的是<a href="https://www.bilibili.com/video/BV1W4cHeZErc" target="_blank">这个视频中</a>PPT的资源文件
    </label><br>
    <label class="checkbox-label">
        <input type="checkbox" name="option" onclick="handleCheckboxClick(this)">
        我知道这是整个工程文件打包
    </label><br>
    <label class="checkbox-label">
        <input type="checkbox" name="option" onclick="handleCheckboxClick(this)">
        我明白视频用的是“组合 合并.pptx”里面的显示屏由其他PPT导出
    </label><br>
    <label class="checkbox-label">
        <input type="checkbox" name="option" onclick="handleCheckboxClick(this)">
        转载请标明出处
    </label><br>
</div>

<!-- 跳转按钮，初始状态下是隐藏的 -->
<button id="submitButton" style="display:none;" onclick="location.href='https://www.123865.com/s/pvgrVv-wEuBh';">
    我要下载！
</button>

<style>
/* 初始样式 */
.checkbox-label {
    padding: 5px;
    margin: 2px 0;
}

/* 已选中的样式 */
.checked-label {
    background-color: #d4edda; /* 绿色背景 */
}
</style>

<!-- 引入SweetAlert2库 -->
<script src="https://cdn.jsdelivr.net/npm/sweetalert2@11"></script>

<script type="text/javascript">
    // 复选框点击事件
    function handleCheckboxClick(checkbox) {
        var label = checkbox.parentElement;
        if (checkbox.checked) {
            label.classList.add('checked-label');
        } else {
            label.classList.remove('checked-label');
        }
        checkAllBoxes();
    }

    // 检查是否所有复选框均被选中，若是则显示下载按钮并启动人机验证
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

        if (allChecked) {
            showImageCaptchaDialog();
        }
    }

    // 用于记录当前用户选择的图片索引
    let selectedImageIndex = null;

    // 点击图片时的处理函数，高亮显示所选图片
    function selectImage(index) {
        const images = document.querySelectorAll('.captcha-image');
        images.forEach((img) => {
            img.style.border = '2px solid transparent';
        });
        const selectedImg = document.getElementById(`img-${index}`);
        selectedImg.style.border = '2px solid green';
        selectedImageIndex = index;
    }

    // 人机验证函数
    function showImageCaptchaDialog() {
        // 图片资源列表（示例内容，请替换为实际链接和描述）
        const imageList = [
            { src: 'https://pic2.ziyuan.wang/user/tanxifei/2025/02/IMG_20250205_214507_a87f7a55dbe9f.jpg', description: '猫' },
            { src: 'https://pic2.ziyuan.wang/user/tanxifei/2025/02/IMG_20250205_214507_a87f7a55dbe9f.jpg', description: '狗' },
            { src: 'https://pic2.ziyuan.wang/user/tanxifei/2025/02/IMG_20250205_214507_a87f7a55dbe9f.jpg', description: '鸟' },
            { src: 'https://pic2.ziyuan.wang/user/tanxifei/2025/02/IMG_20250205_214507_a87f7a55dbe9f.jpg', description: '鱼' },
            { src: 'https://pic2.ziyuan.wang/user/tanxifei/2025/02/IMG_20250205_214507_a87f7a55dbe9f.jpg', description: '兔子' },
            { src: 'https://pic2.ziyuan.wang/user/tanxifei/2025/02/IMG_20250205_214507_a87f7a55dbe9f.jpg', description: '马' }
        ];

        // 随机抽取4张图片（图片总数可能变化，但始终确保数量>4）
        function getRandomImages(arr, n) {
            let copy = arr.slice();
            let result = [];
            for (let i = 0; i < n; i++) {
                let idx = Math.floor(Math.random() * copy.length);
                result.push(copy[idx]);
                copy.splice(idx, 1);
            }
            return result;
        }
        const captchaImages = getRandomImages(imageList, 4);

        // 随机从这4张图片中选择一张作为目标，获取其描述
        const targetIndex = Math.floor(Math.random() * 4);
        const targetDescription = captchaImages[targetIndex].description;

        // 重置选择记录
        selectedImageIndex = null;

        // 构造验证对话框的HTML内容
        let htmlContent = `<p>请选择描述为：“${targetDescription}”的图片</p>`;
        htmlContent += '<div style="display: flex; gap: 10px;">';
        captchaImages.forEach((img, index) => {
            htmlContent += `<img src="${img.src}" alt="${img.description}" class="captcha-image" style="cursor: pointer; border: 2px solid transparent;" onclick="selectImage(${index})" id="img-${index}">`;
        });
        htmlContent += '</div>';

        // 使用SweetAlert2展示人机验证对话框
        Swal.fire({
            title: '人机验证',
            html: htmlContent,
            showCancelButton: true,
            confirmButtonText: '提交',
            cancelButtonText: '取消',
            preConfirm: () => {
                if (selectedImageIndex === null) {
                    Swal.showValidationMessage('请先选择一张图片');
                    return;
                }
                // 返回用户所选图片的描述，用于后续比对
                return captchaImages[selectedImageIndex].description;
            }
        }).then((result) => {
            // 若用户点击取消，则弹出提示重新验证
            if (result.dismiss === Swal.DismissReason.cancel) {
                Swal.fire({
                    title: '验证取消',
                    text: '请重新完成验证。',
                    icon: 'error'
                });
                return;
            }
            // 比对用户所选图片描述与目标描述是否一致
            if (result.value === targetDescription) {
                // 选择正确，返回正确密码
                Swal.fire({
                    title: '恭喜！',
                    text: '您已确认所有信息。\n下载密码：123456',
                    icon: 'success'
                });
            } else {
                // 选择错误，返回错误密码，但仍提示验证通过
                Swal.fire({
                    title: '恭喜！',
                    text: '您已确认所有信息。\n下载密码：654321',
                    icon: 'success'
                });
            }
        });
    }

    // 页面加载完毕后检查复选框状态
    window.onload = function() {
        checkAllBoxes();
    }
</script>
