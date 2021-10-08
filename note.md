# 操作步骤
1. 初始化package.json
    npm init

2. 安装taildwindcss以及它的依赖postcss,autoprefixer
    npm install -D tailwindcss postcss-cli autoprefixer

3. 初始化postcss.config.js和tailwind.config.js文件
    npx tailwind init -p
    这样我们的根目录下就生成这两个文件啦~

4. 新建css文件夹并载入tailwindcss核心部件
    在 css 文件文件中创建 style.css 或者 tailwind.css 文件并加入以下三行
    @tailwind base;
    @tailwind components;
    @tailwind utilities;

5. 在 package.json 中的 scripts 中加入
    "watch": "postcss css/style.css -o dist/style.css --watch"
    或者
    "build": "tailwind build css/tailwind.css -o dist/tailwind.css"

6. npm run watch 或者 npm run build 

7. 每次修改css/style.css|tailwind.css 都需要执行 6 

8. 创建 html 文件并引入 dist 中的 tailwind.css 或者 style.css
    <link rel="stylesheet" href="../dist/tailwind.css">
    或者
    <link rel="stylesheet" href="../dist/style.css">


# 响应式设计
sm 适用于最小宽度为640px的设备
md 适用于最小宽度为768px的设备
lg 适用于最小宽度为1024px的设备
xl 适用于最小宽度为1280px的设备