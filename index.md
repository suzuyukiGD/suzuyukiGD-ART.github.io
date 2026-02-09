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
            background-image: url('picture/Text2.jpg');
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
            background-attachment: fixed;
        }
        
        /* PC端样式 - 使用横版背景图 */
        @media (min-width: 768px) {
            body {
                background-image: url('picture/suzumiya.png');
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
        
        /* 导航栏样式 */
        .navigation {
            background-color: rgba(255, 255, 255, 0.85);
            border-radius: 10px;
            padding: 15px 30px;
            max-width: 900px;
            margin: 20px auto;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
            backdrop-filter: blur(5px);
            position: sticky;
            top: 10px;
            z-index: 100;
        }
        
        .nav-title {
            text-align: center;
            color: #333;
            margin-bottom: 15px;
            font-size: 1.2em;
            font-weight: bold;
        }
        
        .nav-links {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 10px;
        }
        
        .nav-link {
            background: rgba(52, 152, 219, 0.8);
            color: white;
            padding: 8px 16px;
            border-radius: 20px;
            text-decoration: none;
            font-size: 0.95em;
            transition: all 0.3s ease;
            border: 2px solid transparent;
        }
        
        .nav-link:hover {
            background: rgba(41, 128, 185, 0.9);
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }
        
        .nav-link.active {
            background: rgba(231, 76, 60, 0.9);
            border-color: rgba(192, 57, 43, 0.8);
        }
        
        /* 半透明内容容器 */
        .content-box {
            background-color: rgba(255, 255, 255, 0.7);
            border-radius: 15px;
            padding: 30px;
            max-width: 900px;
            margin: 20px auto;
            box-shadow: 0 8px 30px rgba(0, 0, 0, 0.2);
            backdrop-filter: blur(5px);
        }
        
        /* 画师作品区域 */
        .artist-section {
            margin: 40px 0;
            padding: 20px;
            border-radius: 10px;
            background: rgba(255, 255, 255, 0.5);
            scroll-margin-top: 100px; /* 导航栏高度偏移 */
        }
        
        .artist-section:target {
            background: rgba(255, 255, 255, 0.9);
            box-shadow: 0 0 0 3px rgba(52, 152, 219, 0.3);
            animation: highlight 2s ease;
        }
        
        @keyframes highlight {
            0% { background: rgba(255, 255, 255, 0.9); }
            100% { background: rgba(255, 255, 255, 0.5); }
        }
        
        /* 画师标题 */
        .artist-title {
            text-align: center;
            color: #2c3e50;
            margin-bottom: 25px;
            font-size: 2em;
            border-bottom: 2px solid #3498db;
            padding-bottom: 10px;
        }
        
        /* 图片样式 */
        .profile-img {
            display: block;
            max-width: 500px;
            width: 90%;
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
            align-items: center;
            gap: 40px;
            margin: 30px 0;
        }
        
        .gallery-item {
            width: 100%;
            max-width: 600px;
            text-align: center;
        }
        
        /* 图片说明 */
        .image-caption {
            margin-top: 10px;
            color: #666;
            font-style: italic;
            font-size: 0.95em;
        }
        
        /* 返回顶部按钮 */
        .back-to-top {
            display: block;
            text-align: center;
            margin: 30px auto 10px;
            padding: 10px 20px;
            background: rgba(52, 152, 219, 0.8);
            color: white;
            text-decoration: none;
            border-radius: 20px;
            max-width: 150px;
            transition: all 0.3s ease;
        }
        
        .back-to-top:hover {
            background: rgba(41, 128, 185, 0.9);
            transform: translateY(-2px);
        }
        
        /* 响应式调整 */
        @media (max-width: 767px) {
            body {
                padding: 10px;
                background-attachment: scroll;
            }
            
            .navigation {
                padding: 12px 20px;
                margin: 10px auto;
            }
            
            .nav-links {
                gap: 6px;
            }
            
            .nav-link {
                padding: 6px 12px;
                font-size: 0.85em;
            }
            
            .content-box {
                padding: 20px;
                margin: 15px auto;
            }
            
            .artist-title {
                font-size: 1.6em;
            }
            
            .gallery {
                gap: 25px;
            }
        }
    </style>
</head>
<body>  
    <!-- 导航栏 -->
    <div class="navigation">
        <div class="nav-title">画师导航</div>
        <div class="nav-links">
            <a href="#guyikun" class="nav-link active">顾以坤</a>
            <a href="#artist2" class="nav-link">画师二</a>
            <a href="#artist3" class="nav-link">画师三</a>
            <a href="#artist4" class="nav-link">画师四</a>
            <!-- 可以继续添加更多画师 -->
        </div>
    </div>
    
    <!-- 顾以坤作品区域 -->
    <div class="content-box">
        <section id="guyikun" class="artist-section">
            <h2 class="artist-title">顾以坤作品集</h2>
            
            <div class="gallery">
                <div class="gallery-item">
                    <img src="./picture/Yikun Gu1.png" alt="顾以坤作品1" class="profile-img">
                    <div class="image-caption">作品一：春日幻想</div>
                </div>
                <div class="gallery-item">
                    <img src="./picture/Yikun Gu2.jpg" alt="顾以坤作品2" class="profile-img">
                    <div class="image-caption">作品二：凉宫的日常</div>
                </div>
                <!-- 可以添加更多作品 -->
            </div>
            
            <p class="description">
                顾以坤，凉宫春日应援团广东支部成员，擅长绘制动漫同人作品，作品风格清新唯美。
            </p>
            
            <a href="#" class="back-to-top">返回顶部</a>
        </section>
        
        <!-- 其他画师区域（示例） -->
        <section id="artist2" class="artist-section">
            <h2 class="artist-title">画师二作品集</h2>
            <p class="description">更多作品正在筹备中...</p>
            <a href="#" class="back-to-top">返回顶部</a>
        </section>
        
        <section id="artist3" class="artist-section">
            <h2 class="artist-title">画师三作品集</h2>
            <p class="description">更多作品正在筹备中...</p>
            <a href="#" class="back-to-top">返回顶部</a>
        </section>
        
        <section id="artist4" class="artist-section">
            <h2 class="artist-title">画师四作品集</h2>
            <p class="description">更多作品正在筹备中...</p>
            <a href="#" class="back-to-top">返回顶部</a>
        </section>
    </div>
    
    <script>
        // 导航链接点击效果
        document.querySelectorAll('.nav-link').forEach(link => {
            link.addEventListener('click', function() {
                // 移除所有active类
                document.querySelectorAll('.nav-link').forEach(l => {
                    l.classList.remove('active');
                });
                // 给当前点击的链接添加active类
                this.classList.add('active');
            });
        });
        
        // 返回顶部按钮平滑滚动
        document.querySelectorAll('.back-to-top').forEach(button => {
            button.addEventListener('click', function(e) {
                e.preventDefault();
                window.scrollTo({
                    top: 0,
                    behavior: 'smooth'
                });
                // 重置导航栏active状态
                document.querySelectorAll('.nav-link').forEach(l => {
                    l.classList.remove('active');
                });
                document.querySelector('.nav-link[href="#guyikun"]').classList.add('active');
            });
        });
        
        // 监听滚动，高亮当前可见的画师区域
        window.addEventListener('scroll', function() {
            const sections = document.querySelectorAll('.artist-section');
            const navLinks = document.querySelectorAll('.nav-link');
            
            let currentSection = '';
            
            sections.forEach(section => {
                const sectionTop = section.offsetTop - 150;
                const sectionHeight = section.clientHeight;
                if (window.scrollY >= sectionTop && window.scrollY < sectionTop + sectionHeight) {
                    currentSection = section.getAttribute('id');
                }
            });
            
            navLinks.forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('href').substring(1) === currentSection) {
                    link.classList.add('active');
                }
            });
        });
        
        // 设备检测
        function updateDeviceInfo() {
            const width = window.innerWidth;
            const isMobile = width < 768;
            console.log(`设备: ${isMobile ? '移动端' : 'PC端'} (${width}×${window.innerHeight})`);
        }
        
        window.addEventListener('load', updateDeviceInfo);
        window.addEventListener('resize', updateDeviceInfo);
    </script>
</body>
</html>


































































































