# Lss2209010046
在该库根目录下创建一个readme.md文件，文件内容本人求职简历，除了姓名和学号以外，求职简历的其他信息均可由虚构； 3. 在github上检索"Data-Science-Handbook仓库"，fork后并clone到本地D盘以自己名字拼音命名的文件夹下； 4. 在github上检索"ython-100-Days"仓库，fork后并clone到本地D盘以自己名字拼音命名的文件夹下； 5. 使用jupyte note打开Data-Science-Handbook库中的“python_Data_Science_Handbook-master\notebook\05.02-Scikit-Learn简介.ipynb“文件。
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>个人求职简历</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 0;
            background-color: #f4f4f9;
        }
        .container {
            width: 80%;
            max-width: 800px;
            margin: 20px auto;
            background: #fff;
            padding: 20px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            position: relative;
        }
        h1, h2, h3 {
            color: #333;
        }
        ul {
            list-style-type: none;
            padding: 0;
        }
        li {
            margin-bottom: 10px;
        }
        .header, .section {
            margin-bottom: 20px;
            border-bottom: 1px solid #ccc;
            padding-bottom: 10px;
        }
        .photo-container {
            position: absolute;
            top: 20px;
            right: 20px;
            width: 150px;
            height: 150px;
            border: 2px dashed #ccc;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 1;
        }
        #photo {
            width: 100%;
            height: 100%;
            object-fit: cover;
            border-radius: 50%;
            display: none;
            cursor: move;
            position: absolute;
        }
        #upload-label {
            color: #666;
            font-size: 14px;
            text-align: center;
            padding: 10px;
        }
        #photo-input {
            display: none;
        }
        .header-content {
            margin-right: 170px; /* 给照片留出空间 */
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="photo-container">
            <input type="file" id="photo-input" accept="image/*">
            <label for="photo-input" id="upload-label">点击上传证件照<br>(150x150像素)</label>
            <img id="photo" src="" alt="个人照片">
        </div>
        <div class="header">
            <div class="header-content">
                <h1>个人求职简历</h1>
                <p><strong>姓名：</strong>雷思思</p>
                <p><strong>学号：</strong>2209010046</p>
                <p><strong>联系方式：</strong>123-456-7890 | <a href="mailto:zhangsan@example.com">zhangsan@example.com</a></p>
                <p><strong>地址：</strong>某某市某某区某某路123号</p>
            </div>
        </div>
        <div class="section">
            <h2>教育背景</h2>
            <ul>
                <li>
                    <p><strong>某某大学</strong> - 计算机科学与技术</p>
                    <p>本科 | 2015年9月 - 2019年6月</p>
                    <p>主修课程：数据结构、算法设计与分析、数据库系统、计算机网络等</p>
                </li>
            </ul>
        </div>
        <div class="section">
            <h2>工作经验</h2>
            <ul>
                <li>
                    <p><strong>某某科技有限公司</strong> - 前端开发工程师</p>
                    <p>2019年7月 - 至今</p>
                    <ul>
                        <li>负责公司前端项目的开发，使用HTML5、CSS3、JavaScript等技术</li>
                        <li>与后端团队合作，通过API接口实现前后端数据交互</li>
                        <li>优化页面性能，提高用户体验</li>
                        <li>参与项目需求分析、设计和编码实现</li>
                    </ul>
                </li>
            </ul>
        </div>
        <div class="section">
            <h2>技能</h2>
            <ul>
                <li>熟练掌握HTML5、CSS3、JavaScript等前端技术</li>
                <li>熟悉React、Vue等前端框架</li>
                <li>了解Node.js后端技术</li>
                <li>熟练使用Git进行版本控制</li>
                <li>具备良好的问题解决能力和团队合作精神</li>
            </ul>
        </div>
    </div>
    <script>
        const photoInput = document.getElementById('photo-input');
        const photo = document.getElementById('photo');
        const uploadLabel = document.getElementById('upload-label');
        photoInput.addEventListener('change', function(event) {
            const file = event.target.files[0];
            if (file) {
                const reader = new FileReader();
                reader.onload = function(e) {
                    photo.src = e.target.result;
                    photo.style.display = 'block';
                    uploadLabel.style.display = 'none';
                };
                reader.readAsDataURL(file);
            }
        });
        // 拖动功能
        let isDragging = false;
        let startX = 0;
        let startY = 0;
        let initialX = 0;
        let initialY = 0;
        photo.addEventListener('mousedown', function(e) {
            isDragging = true;
            startX = e.clientX;
            startY = e.clientY;
            initialX = photo.offsetLeft;
            initialY = photo.offsetTop;
            photo.style.cursor = 'grabbing';
        });
        document.addEventListener('mousemove', function(e) {
            if (isDragging) {
                e.preventDefault();
                const dx = e.clientX - startX;
                const dy = e.clientY - startY;
                photo.style.left = initialX + dx + 'px';
                photo.style.top = initialY + dy + 'px';
            }
        });
        document.addEventListener('mouseup', function() {
            isDragging = false;
            photo.style.cursor = 'move';
        });
    </script>
</body>
</html>
