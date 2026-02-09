<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>凉宫春日应援团广东支部画作展示</title>
    <style>
        /* 基础样式 */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 20px;
            min-height: 100vh;
            background-color: #f0f0f0; /* 备用背景色 */
        }
        
        /* 移动端样式（默认）- 使用竖版背景图 */
        body {
            background-image: url('picture/Text2.jpg'); /* 竖版图片 */
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
            background-attachment: fixed;
        }
        
        /* PC端样式 - 使用横版背景图 */
        @media (min-width: 768px) {
            body {
                background-image: url('picture/suzumiya.png'); /* 横版图片 */
                background-size: cover;
                background-position: center;
                background-repeat: no-repeat;
                background-attachment: fixed;
            }
        }
        
        /* 大屏幕PC优化 */
        @media (min-width: 1200px) {
            body {
                background-position: center 40%;
            }
        }
        
        /* 半透明内容容器 */
        .content-box {
            background-color: rgba(255, 255, 255, 0.7); /* 白色半透明背景 */
            border-radius: 15px; /* 圆角 */
            padding: 30px; /* 内边距 */
            max-width: 900px; /* 最大宽度 */
            margin: 50px auto; /* 居中 */
            box-shadow: 0 8px 30px rgba(0, 0, 0, 0.2); /* 阴影效果 */
            backdrop-filter: blur(5px); /* 毛玻璃效果 */
        }
        
        /* 标题样式 */
        h1 {
            text-align: center;
            color: #333;
            margin-bottom: 10px;
            font-size: 2.5em;
        }
        
        h2 {
            text-align: center;
            color: #555;
            margin-bottom: 30px;
            font-size: 1.8em;
        }
        
        /* 图片样式 */
        .profile-img {
            display: block;
            max-width: 500px;
            width: 90%；
            margin: 20px auto;
            border-radius: 10px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }
        
        .profile-img:hover {
            transform: scale(1.02);
        }
        
        /* 图片容器，用于多张图片布局 */
        .gallery {
            display: flex;
            flex-direction: column;
            align*items: center;
            gap: 40px;
            margin: 30px 0;
        }
        
        .gallery-item {
            width: 100%;
            max-width: 600%;
            text_align: center;
        }
        
        /* 段落样式 */
        .description {
            text-align: justify;
            text-justify: inter-word;
            line-height: 1.8;
            margin: 30px 0;
            padding: 0 20px;
            color: #444;
            font-size: 1.1em;
        }
        
        /* 响应式调整 */
        @media (max-width: 767px) {
            body {
                padding: 10px;
                background-attachment: scroll; /* 移动端取消固定，提高性能 */
            }
            
            .content-box {
                padding: 20px;
                margin: 20px auto;
                border-radius: 10px;
            }
            
            h1 {
                font-size: 2em;
            }
            
            h2 {
                font-size: 1.5em;
            }
            
            .gallery {
                gap: 15px;
            }
        }
        
        /* 装饰分隔线 */
        .divider {
            height: 2px;
            background: linear-gradient(to right, transparent, #3498db, transparent);
            margin: 30px auto;
            max-width: 200px;
        }
    </style>
</head>
<body>  
    <!-- 半透明内容框开始 -->
    <div class="content-box">
        <h1>广东支部画作展示</h1>
        <h2>顾以坤</h2>
        
        <!-- 装饰分隔线 -->
        <div class="divider"></div>
        
        <!-- 图片画廊 -->
        <div class="gallery">
            <div class="gallery-item">
                <img src="./picture/Yikun Gu1.png" alt="顾以坤作品1" class="profile-img">
            </div>
            <div class="gallery-item">
                <img src="./picture/Yikun Gu2.jpg" alt="顾以坤作品2" class="profile-img">
            </div>
        </div>
        
        <!-- 装饰分隔线 -->
        <div class="divider"></div>
        
        <p class="description">
            This is a test site and is not yet complete.
        </p>
    </div> <!-- 关闭 content-box -->
    
    <!-- 设备检测提示（可选） -->
    <div id="device-notice" style="
        position: fixed;
        bottom: 10px;
        right: 10px;
        background: rgba(0,0,0,0.7);
        color: white;
        padding: 5px 10px;
        border-radius: 5px;
        font-size: 12px;
        display: none;
    ">
        当前设备：<span id="device-type"></span>
    </div>
    
    <script>
        // 设备检测和提示
        function updateDeviceInfo() {
            const width = window.innerWidth;
            const isMobile = width < 768;
            const deviceType = isMobile ? '移动端 (竖版背景)' : 'PC端 (横版背景)';
            
            // 更新提示信息
            document.getElementById('device-type').textContent = deviceType;
            
            // 控制台输出调试信息
            console.log(`窗口尺寸: ${width}×${window.innerHeight}`);
            console.log(`当前背景: ${isMobile ? 'picture/Text1-vertical.jpeg' : 'picture/Text1-horizontal.jpeg'}`);
            
            // 显示设备提示（3秒后自动隐藏）
            const notice = document.getElementById('device-notice');
            notice.style.display = 'block';
            setTimeout(() => {
                notice.style.display = 'none';
            }, 3000);
        }
        
        // 页面加载时初始化
        window.addEventListener('load', function() {
            updateDeviceInfo();
            checkBackgroundImages();
        });
        
        // 窗口大小变化时更新
        window.addEventListener('resize', updateDeviceInfo);
        
        // 如果只有一张图，取消下面这行的注释
        // useSingleBackground();
    </script>
</body>
</html>































































































