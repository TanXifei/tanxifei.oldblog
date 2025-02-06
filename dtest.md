---
layout: post
title:  "上三通配化PPT资源下载"
date:   2025-02-04
excerpt: "你是不是要下载？往下看"
image: "https://pic2.ziyuan.wang/user/tanxifei/2024/11/29_eee5fe351e766.jpg"
---

<audio controls autoplay>
  <source src="https://m801.music.126.net/20250207004335/d6e9c05a47452a45d2006573c6006b8e/jdymusic/obj/w5zDlMODwrDDiGjCn8Ky/2409337666/9e86/ecde/a791/d893843cfac4b08ff727bb0b871267c1.flac?vuutv=ILkueA6TzDaVaJfQubRtiHlhXTO7BC4kGVhVLf1MtvzflfTiZ1ibmsOkTYJjv3A9wJvns44SH0Ic1hljqkEqLaiwlUDK6AjuErzdKZVHJSA=" type="audio/mpeg">
  Your browser does not support the audio element.
</audio>
# 请务必仔细阅读说明

## 工程文件夹整体打包 不提供使用方法 请自行研究

## 内显“司机” “检修”过于复杂 能力限制没有制作

### 制作外显/内显界面时 建议复制全显进行修改

### 导出外显/内显图片时 请将背景替换为黑色 便于嵌入
<!-- 下载PPT资源文件 -->

#### 请确认以下信息:

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


<style>
/* 复选框样式 */
.checkbox-label {
    padding: 5px;
    margin: 2px 0;
}

/* 已选中的复选框样式 */
.checked-label {
    background-color: #66CCFF;
}

/* 验证图片选中样式 */
.selected-image {
    border: 2px solid green !important;
}

/* 图片容器样式：使用flexbox实现自动适应布局 */
.captcha-image-container {
    display: flex;
    flex-wrap: wrap;           /* 允许换行 */
    justify-content: space-between;  /* 图片均匀分布 */
    gap: 10px;               /* 图片间距 */
    width: 100%;
    box-sizing: border-box;
}

/* 每张图片占据相等的宽度，并自适应窗口大小 */
.captcha-image {
    flex: 1 1 30%;                  /* 每张图片占据30%的宽度，且在小屏幕上会自动调整 */
    max-width: 150px;               /* 限制图片最大宽度 */
    height: auto;                   /* 高度自适应 */
    cursor: pointer;
    object-fit: cover;              /* 保持图片比例 */
    min-width: 120px;               /* 确保图片最小宽度，避免过小 */
}

/* 图片容器不超出视口宽度 */
.captcha-image-container > div {
    display: flex;
    justify-content: center;
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

    // 检查所有复选框是否均已勾选，若是则显示下载按钮并启动人机验证
    function checkAllBoxes() {
        var checkboxes = document.querySelectorAll('input[name="option"]');

        var allChecked = true;
        for (var i = 0; i < checkboxes.length; i++) {
            if (!checkboxes[i].checked) {
                allChecked = false;
                break;
            }
        }


        if (allChecked) {
            showImageCaptchaDialog();
        }
    }

    // 存储当前验证对话框中用户选中的图片索引数组
    let selectedIndices = [];

    // 用户点击图片时的处理函数：实现多选/反选，并更新样式
    function toggleImageSelection(index) {
        const imgElem = document.getElementById(`img-${index}`);
        const pos = selectedIndices.indexOf(index);
        if (pos === -1) {
            // 未选中则添加
            selectedIndices.push(index);
            imgElem.classList.add('selected-image');
        } else {
            // 已选中则取消选中
            selectedIndices.splice(pos, 1);
            imgElem.classList.remove('selected-image');
        }
    }

    // 人机验证函数
    function showImageCaptchaDialog() {
        // 图片资源列表，每个对象包含图片链接及一个描述数组
        const imageList = [
            { src: 'https://img.erpweb.eu.org/imgs/2025/02/217a7dae71138e3c.png', descriptions: ['三菱电机', '日本原装LCD'] },
            { src: 'https://img.erpweb.eu.org/imgs/2025/02/c76ff2a5963ccf02.png', descriptions: ['三菱电机'] },
            { src: 'https://img.erpweb.eu.org/imgs/2025/02/b252eeae4baac7e6.png', descriptions: ['三菱电机', '日本原装LCD'] },
            { src: 'https://img.erpweb.eu.org/imgs/2025/02/708fbd5e0b7a2972.png', descriptions: ['三菱电机'] },
            { src: 'https://img.erpweb.eu.org/imgs/2025/02/af99d1fff5d8ef4a.png', descriptions: ['上海三菱'] },
            { src: 'https://img.erpweb.eu.org/imgs/2025/02/7579d639be0d0ae8.png', descriptions: ['三菱电机'] },
            { src: 'https://img.erpweb.eu.org/imgs/2025/02/b782b204b51807fb.png', descriptions: ['三菱电机', '日本原装LCD'] },

            { src: 'https://img.erpweb.eu.org/imgs/2025/02/32af2c9b1372de4e.png', descriptions: ['三菱电机'] },
            { src: 'https://pic2.ziyuan.wang/user/tanxifei/2025/02/Screenshot_20250206_001835_ffb701489b076.jpg', descriptions: ['上海三菱'] },
            { src: 'https://pic2.ziyuan.wang/user/tanxifei/2025/02/Screenshot_20250206_001902_67e0d6af2e94e.jpg', descriptions: ['三菱电机'] },
            { src: 'https://pic2.ziyuan.wang/user/tanxifei/2025/02/IMG_20250206_001848_4cc35c4747ebb.png', descriptions: ['三菱电机'] },
            { src: 'https://img.erpweb.eu.org/imgs/2025/02/48d174689dd8b275.png', descriptions: ['三菱电机'] },
            { src: 'https://img.erpweb.eu.org/imgs/2025/02/8819543e0f406e54.png', descriptions: ['三菱电机'] }
        ];

        // 随机抽取6张图片（确保图片库数量始终大于6）
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
        const captchaImages = getRandomImages(imageList, 6);

        // 从6张图片中随机选择1张，并抽取1或2个描述作为提问条件
        const randomImage = captchaImages[Math.floor(Math.random() * captchaImages.length)];
        const targetDescriptions = [];

        // 从选中的图片的描述中随机抽取1到2个描述
        targetDescriptions.push(randomImage.descriptions[Math.floor(Math.random() * randomImage.descriptions.length)]);
        if (Math.random() < 0.5 && randomImage.descriptions.length > 1) {
            // 如果描述有多个并且随机选择了两个描述
            const secondDesc = randomImage.descriptions.find(d => d !== targetDescriptions[0]);
            targetDescriptions.push(secondDesc);
        }

        // 计算正确答案的图片索引集合：
        // 正确图片是指其描述数组包含【所有】目标描述
        let correctIndices = [];
        captchaImages.forEach((img, index) => {
            let hasAll = targetDescriptions.every(desc => img.descriptions.includes(desc));
            if (hasAll) {
                correctIndices.push(index);
            }
        });

        // 重置用户选择记录
        selectedIndices = [];

        // 构造验证对话框的HTML内容
        let questionText = '请选择所有包含描述：';
        if (targetDescriptions.length === 1) {
            questionText += `“${targetDescriptions[0]}”的图片`;
        } else {
            questionText += `“${targetDescriptions.join('” 和 “')}”的图片`;
        }
        let htmlContent = `<p>${questionText}</p>`;
        htmlContent += '<div class="captcha-image-container">';
        captchaImages.forEach((img, index) => {
            htmlContent += `
                <div class="captcha-image-container" style="cursor: pointer;" onclick="toggleImageSelection(${index})">
                    <img src="${img.src}" alt="${img.descriptions.join(', ')}" class="captcha-image" id="img-${index}">
                    <!-- 已删除描述文本部分 -->
                </div>
            `;
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
                return selectedIndices;
            }
        }).then((result) => {
            if (result.dismiss === Swal.DismissReason.cancel) {
                Swal.fire({
                    title: '验证取消',
                    text: '请重新完成验证。',
                    icon: 'error'
                });
                return;
            }
            // 对用户选中的索引数组和正确答案数组进行排序后比对
            const userSelection = result.value.sort((a, b) => a - b);
            const correctSorted = correctIndices.sort((a, b) => a - b);
            if (JSON.stringify(userSelection) === JSON.stringify(correctSorted)) {
                // 验证正确，返回正确密码
                Swal.fire({
                    title: '哦.',
                    text: '您已通过人机验证。\n点击下方按钮下载',
                    icon: 'success',
                    confirmButtonText: '前往下载'
                  }).then((result) => {
                    if (result.isConfirmed) {
                        window.location.href = 'https://mis1072-my.sharepoint.com/:u:/g/personal/tanxifei_mis1072_top/EU37wwmfJthKjKKKbyXZRJABJpFLd0S9H5CwD2FeGjMinw?e=3L4e25';
                    }
                });
            } else {
                // 验证错误，返回错误密码，但提示验证通过
                Swal.fire({
                    title: '哦',
                    text: '您已通过人机验证。\n点击下方按钮下载',
                    icon: 'success',
                    confirmButtonText: '前往下载'
                  }).then((result) => {
                    if (result.isConfirmed) {
                        window.location.href = 'https://mis1072-my.sharepoint.com/:u:/g/personal/tanxifei_mis1072_top/Ea0YNge3X0hMhXDxquDWKTIBwRLRkKfmxD_W5-BD7BcK9Q?e=PJYfcm';
                    }
                });
            }
        });
    }
</script>
