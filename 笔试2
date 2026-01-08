<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Figma - 前端工程师（实习）</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
        }
        
        body {
            background-color: #f8f9fa;
            color: #333;
            line-height: 1.6;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
        }
        
        /* 状态栏样式 */
        .status-bar {
            background-color: #fff;
            padding: 10px 15px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-size: 14px;
            border-bottom: 1px solid #eee;
        }
        
        .status-left {
            display: flex;
            align-items: center;
            gap: 5px;
        }
        
        .status-right {
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .vpn-indicator {
            background-color: #e3f2fd;
            color: #1976d2;
            padding: 2px 6px;
            border-radius: 4px;
            font-size: 12px;
        }
        
        /* 头部样式 */
        .header {
            background-color: #fff;
            padding: 20px 15px;
            text-align: center;
            border-bottom: 1px solid #eee;
        }
        
        .logo {
            font-weight: 700;
            font-size: 24px;
            color: #0d0d0d;
            margin-bottom: 8px;
        }
        
        .title {
            font-size: 18px;
            color: #333;
            font-weight: 500;
        }
        
        /* 主要内容区域 */
        .main-content {
            flex: 1;
            padding: 30px 20px;
            max-width: 1200px;
            margin: 0 auto;
            width: 100%;
        }
        
        .upload-container {
            display: flex;
            flex-direction: row;
            background-color: #fff;
            border-radius: 16px;
            overflow: hidden;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
            min-height: 400px;
        }
        
        /* 左侧区域 */
        .left-panel {
            flex: 1;
            background-color: #f0f7ff;
            padding: 40px 30px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
        }
        
        .cat-illustration {
            width: 160px;
            height: 160px;
            background-color: #1976d2;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            margin-bottom: 25px;
        }
        
        .cat-icon {
            font-size: 80px;
            color: white;
        }
        
        .finish-text {
            font-size: 28px;
            font-weight: 700;
            color: #0d0d0d;
            margin-bottom: 10px;
        }
        
        .upload-text {
            font-size: 18px;
            color: #666;
            font-weight: 500;
        }
        
        /* 右侧区域 */
        .right-panel {
            flex: 1;
            padding: 40px 30px;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }
        
        .step-indicator {
            color: #1976d2;
            font-weight: 600;
            font-size: 14px;
            margin-bottom: 25px;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .step-indicator i {
            font-size: 12px;
        }
        
        .upload-area {
            border: 2px dashed #c5c5c5;
            border-radius: 12px;
            padding: 40px 20px;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s ease;
            background-color: #fafafa;
            margin-bottom: 25px;
        }
        
        .upload-area:hover {
            border-color: #1976d2;
            background-color: #f0f7ff;
        }
        
        .upload-area.dragover {
            border-color: #1976d2;
            background-color: #e3f2fd;
        }
        
        .upload-icon {
            font-size: 48px;
            color: #888;
            margin-bottom: 15px;
        }
        
        .upload-area:hover .upload-icon {
            color: #1976d2;
        }
        
        .upload-instruction {
            font-size: 16px;
            color: #555;
            margin-bottom: 8px;
        }
        
        .upload-subtext {
            font-size: 14px;
            color: #888;
        }
        
        .file-input {
            display: none;
        }
        
        .file-name {
            margin-top: 15px;
            font-size: 14px;
            color: #1976d2;
            font-weight: 500;
            word-break: break-all;
        }
        
        .skip-text {
            font-size: 14px;
            color: #888;
            text-align: center;
            margin-bottom: 30px;
        }
        
        .skip-text a {
            color: #1976d2;
            text-decoration: none;
            font-weight: 500;
        }
        
        .skip-text a:hover {
            text-decoration: underline;
        }
        
        /* 按钮区域 */
        .button-container {
            display: flex;
            gap: 15px;
            margin-top: 10px;
        }
        
        .btn {
            padding: 14px 28px;
            border-radius: 8px;
            font-size: 16px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            border: none;
            flex: 1;
            text-align: center;
        }
        
        .btn-step {
            background-color: #f0f0f0;
            color: #666;
        }
        
        .btn-step:hover {
            background-color: #e5e5e5;
        }
        
        .btn-finish {
            background-color: #1976d2;
            color: white;
        }
        
        .btn-finish:hover {
            background-color: #1565c0;
        }
        
        .btn-finish:disabled {
            background-color: #b0b0b0;
            cursor: not-allowed;
        }
        
        /* 底部导航 */
        .footer-nav {
            background-color: #fff;
            border-top: 1px solid #eee;
            padding: 20px 15px;
            display: flex;
            justify-content: center;
            gap: 30px;
        }
        
        .nav-link {
            color: #666;
            text-decoration: none;
            font-size: 16px;
            font-weight: 500;
            padding: 8px 0;
            position: relative;
        }
        
        .nav-link:hover {
            color: #1976d2;
        }
        
        /* 响应式设计 */
        @media (max-width: 768px) {
            .upload-container {
                flex-direction: column;
            }
            
            .left-panel, .right-panel {
                padding: 30px 20px;
            }
            
            .cat-illustration {
                width: 120px;
                height: 120px;
            }
            
            .cat-icon {
                font-size: 60px;
            }
            
            .finish-text {
                font-size: 24px;
            }
            
            .upload-text {
                font-size: 16px;
            }
            
            .button-container {
                flex-direction: column;
            }
            
            .btn {
                width: 100%;
            }
        }
        
        /* 成功状态 */
        .success-message {
            display: none;
            background-color: #e8f5e9;
            color: #2e7d32;
            padding: 15px;
            border-radius: 8px;
            margin-top: 20px;
            text-align: center;
            font-weight: 500;
        }
    </style>
</head>
<body>
    <!-- 状态栏 -->
    <div class="status-bar">
        <div class="status-left">
            <span>15:42</span>
        </div>
        <div class="status-right">
            <span class="vpn-indicator">VPN</span>
            <span>5G</span>
            <i class="fas fa-signal"></i>
            <i class="fas fa-battery-full"></i>
        </div>
    </div>
    
    <!-- 头部 -->
    <header class="header">
        <div class="logo">Figma</div>
        <h1 class="title">前端工程师（实习）</h1>
    </header>
    
    <!-- 主要内容 -->
    <main class="main-content">
        <div class="upload-container">
            <!-- 左侧面板 -->
            <div class="left-panel">
                <div class="cat-illustration">
                    <i class="fas fa-cat cat-icon"></i>
                </div>
                <div class="finish-text">Finish!</div>
                <div class="upload-text">Upload Your Resume</div>
            </div>
            
            <!-- 右侧面板 -->
            <div class="right-panel">
                <div class="step-indicator">
                    <i class="fas fa-flag"></i>
                    Last step
                </div>
                
                <!-- 上传区域 -->
                <div class="upload-area" id="uploadArea">
                    <i class="fas fa-cloud-upload-alt upload-icon"></i>
                    <div class="upload-instruction">
                        Drag your resume file to this area, or click on the area to select the appropriate file to upload
                    </div>
                    <div class="upload-subtext">
                        Supports PDF, DOC, DOCX up to 5MB
                    </div>
                    <div class="file-name" id="fileName"></div>
                    <input type="file" id="fileInput" class="file-input" accept=".pdf,.doc,.docx">
                </div>
                
                <!-- 跳过提示 -->
                <div class="skip-text">
                    can also <a href=" " id="skipLink">skip this step</a >
                </div>
                
                <!-- 按钮 -->
                <div class="button-container">
                    <button class="btn btn-step" id="backBtn">
                        <i class="fas fa-arrow-left"></i> Last step
                    </button>
                    <button class="btn btn-finish" id="finishBtn" disabled>Finish</button>
                </div>
                
                <!-- 成功消息 -->
                <div class="success-message" id="successMessage">
                    <i class="fas fa-check-circle"></i> Resume uploaded successfully!
                </div>
            </div>
        </div>
    </main>
    
    <!-- 底部导航 -->
    <footer class="footer-nav">
        <a href="#" class="nav-link">Sign up</a >
        <a href="#" class="nav-link">Log in</a >
    </footer>

    <script>
        // DOM元素
        const uploadArea = document.getElementById('uploadArea');
        const fileInput = document.getElementById('fileInput');
        const fileName = document.getElementById('fileName');
        const finishBtn = document.getElementById('finishBtn');
        const skipLink = document.getElementById('skipLink');
        const backBtn = document.getElementById('backBtn');
        const successMessage = document.getElementById('successMessage');
        
        // 点击上传区域触发文件选择
        uploadArea.addEventListener('click', () => {
            fileInput.click();
        });
        
        // 处理文件选择
        fileInput.addEventListener('change', (e) => {
            if (e.target.files.length > 0) {
                const file = e.target.files[0];
                const fileSize = (file.size / (1024 * 1024)).toFixed(2); // MB
                
                // 检查文件类型和大小
                const validTypes = ['application/pdf', 'application/msword', 'application/vnd.openxmlformats-officedocument.wordprocessingml.document'];
                const maxSize = 5; // 5MB
                
                if (!validTypes.includes(file.type)) {
                    alert('Please select a valid file type (PDF, DOC, DOCX).');
                    fileInput.value = '';
                    return;
                }
                
                if (file.size > maxSize * 1024 * 1024) {
                    alert(`File size exceeds ${maxSize}MB limit.`);
                    fileInput.value = '';
                    return;
                }
                
                // 显示文件名并启用Finish按钮
                fileName.textContent = `Selected: ${file.name} (${fileSize} MB)`;
                finishBtn.disabled = false;
            }
        });
        
        // 拖放功能
        uploadArea.addEventListener('dragover', (e) => {
            e.preventDefault();
            uploadArea.classList.add('dragover');
        });
        
        uploadArea.addEventListener('dragleave', () => {
            uploadArea.classList.remove('dragover');
        });
        
        uploadArea.addEventListener('drop', (e) => {
            e.preventDefault();
            uploadArea.classList.remove('dragover');
            
            if (e.dataTransfer.files.length > 0) {
                fileInput.files = e.dataTransfer.files;
                const event = new Event('change', { bubbles: true });
                fileInput.dispatchEvent(event);
            }
        });
        
        // Finish按钮点击事件
        finishBtn.addEventListener('click', () => {
            if (!finishBtn.disabled) {
                successMessage.style.display = 'block';
                finishBtn.disabled = true;
                finishBtn.textContent = 'Submitted';
                
                // 模拟提交后的状态
                setTimeout(() => {
                    alert('Application submitted successfully!');
                }, 500);
            }
        });
        
        // 跳过链接点击事件
        skipLink.addEventListener('click', (e) => {
            e.preventDefault();
            if (confirm('Are you sure you want to skip uploading your resume?')) {
                fileName.textContent = 'Skipped - No resume uploaded';
                finishBtn.disabled = false;
            }
        });
        
        // 返回上一步按钮
        backBtn.addEventListener('click', () => {
            alert('This would navigate to the previous step in a real application.');
        });
        
        // 底部导航链接
        document.querySelectorAll('.nav-link').forEach(link => {
            link.addEventListener('click', (e) => {
                e.preventDefault();
                alert(`This would navigate to ${e.target.textContent} page in a real application.`);
            });
        });
    </script>
</body>
</html>
