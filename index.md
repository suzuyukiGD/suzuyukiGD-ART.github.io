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
            background-color: #f0f0f0;
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
        
        /* 半透明内容容器 - 竖版窄布局 */
        .content-box {
            background-color: rgba(255, 255, 255, 0.75);
            border-radius: 15px;
            padding: 30px;
            max-width: 500px; /* 窄布局，适合竖版 */
            margin: 40px auto;
            box-shadow: 0 8px 30px rgba(0, 0, 0, 0.2);
            backdrop-filter: blur(5px);
        }
        
        /* 标题样式 */
        h1 {
            text-align: center;
            color: #333;
            margin-bottom: 10px;
            font-size: 2.2em;
        }
        
        h2 {
            text-align: center;
            color: #555;
            margin-bottom: 25px;
            font-size: 1.6em;
        }
        
        /* 图片容器 - 垂直排列 */
        .image-gallery {
            display: flex;
            flex-direction: column; /* 垂直排列 */
            align-items: center;
            gap: 25px; /* 图片之间的间距 */
            margin: 25px 0;
        }
        
        /* 单张图片样式 */
        .artwork-img {
            display: block;
            max-width: 320px; /* 固定最大宽度 */
            width: 90%; /* 响应式宽度 */
            border-radius: 10px;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.15);
            transition: transform 0.3s ease;
        }
        
        .artwork-img:hover {
            transform: translateY(-3px);
        }
        
        /* 图片标题（可选） */
        .img-caption {
            text-align: center;
            color: #666;
            font-size: 0.9em;
            margin-top: 8px;
            font-style: italic;
        }
        
        /* 段落样式 */
        .description {
            text-align: justify;
            text-justify: inter-word;
            line-height: 1.7;
            margin: 25px 0;
            padding: 0 15px;
            color: #444;
            font-size: 1.05em;
        }
        
        /* 装饰分隔线 */
        .divider {
            height: 1px;
            background: linear-gradient(to right, 
                transparent, 
                rgba(0, 0, 0, 0.2), 
                transparent
            );
            margin: 20px auto;
            width: 80%;
        }
        
        /* 响应式调整 */
        @media (max-width: 767px) {
            body {
                padding: 15px;
                background-attachment: scroll;
            }
            
            .content-box {
                padding: 25px 20px;
                margin: 25px auto;
                max-width: 90%;
            }
            
            h1 {
                font-size: 1.9em;
            }
            
            h2 {
                font-size: 1.4em;
            }
            
            .artwork-img {
                max-width: 280px;
            }
            
            .image-gallery {
                gap: 20px;
            }
        }
        
        /* PC端优化 */
        @media (min-width: 1200px) {
            .content-box {
                max-width: 450px; /* PC端可以更窄一些 */
            }
            
            .artwork-img {
                max-width: 300px;
            }
        }
    </style>
</head>
<body>  
    <!-- 半透明内容框 -->
    <div class="content-box">
        <h1>广东支部画作展示</h1>
        <h2>顾以坤</h2>
        
        <!-- 装饰分隔线 -->
        <div class="divider"></div>
        
        <!-- 图片垂直排列画廊 -->
        <div class="image-gallery">
            <!-- 作品1 -->
            <div class="artwork-item">
                <img src="./picture/Yikun Gu1.png" alt="顾以坤作品1" class="artwork-img">
                <div class="img-caption">作品一</div>
            </div>
            
            <!-- 作品2 -->
            <div class="artwork-item">
                <img src="./picture/Yikun Gu2.jpg" alt="顾以坤作品2" class="artwork-img">
                <div class="img-caption">作品二</div>
            </div>
        </div>
        
        <!-- 装饰分隔线 -->
        <div class="divider"></div>
        
        <p class="description">
            This is a test site and is not yet complete.
        </p>
    </div>
    
    <!-- 设备检测和背景图检查 -->
    <script>
        // 检查背景图片是否存在
        function checkBackgroundImages() {
            const isMobile = window.innerWidth < 768;
            const bgUrl = isMobile ? 'picture/Text1-vertical.jpeg' : 'picture/Text1-horizontal.jpeg';
            
            const img = new Image();
            img.onload = function() {
                console.log(`✅ 背景图加载成功: ${bgUrl}`);
            };
            img.onerror = function() {
                console.warn(`❌ 背景图可能不存在: ${bgUrl}`);
                // 如果指定的图片不存在，使用通用背景
                document.body.style.backgroundImage = "url('picture/Text1.jpeg')";
                console.log('使用通用背景图: picture/Text1.jpeg');
            };
            img.src = bgUrl;
        }
        
        // 显示当前设备信息
        function showDeviceInfo() {
            const width = window.innerWidth;
            const isMobile = width < 768;
            console.log(`设备: ${isMobile ? '移动端' : 'PC端'} (${width}×${window.innerHeight})`);
            console.log(`背景: ${isMobile ? '竖版' : '横版'}图片`);
        }
        
        // 页面加载时执行
        window.addEventListener('load', function() {
            checkBackgroundImages();
            showDeviceInfo();
        });
        
        // 窗口大小变化时重新检查
        window.addEventListener('resize', function() {
            checkBackgroundImages();
            showDeviceInfo();
        });
        
        // 如果暂时只有一张背景图，可以取消下面代码的注释
        // function useSingleBackground() {
        //     document.body.style.backgroundImage = "url('picture/Text1.jpeg')";
        //     console.log('使用单张背景图模式');
        // }
        // useSingleBackground();
    </script>
</body>
</html>





























































































