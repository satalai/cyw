
动漫人物展示网页
该项目是一个展示动漫角色的网页，采用了简洁的 HTML、CSS 和 JavaScript 技术，支持滚动视差效果，能够直观地呈现角色及相关背景信息。

功能特色
1. 动漫人物展示
展示四位动漫角色的基本信息。
每个角色卡片均包含：
角色形象图片
角色英文名字
角色日文名字及注解
2. 滚动视差背景
页面包含四段滚动视差效果，每段展示不同的背景图片和标题内容。
每段内容均以日语主题与背景相匹配，提升视觉体验。
3. 动态标题交互
鼠标悬浮在页面标题上时，触发特效（添加 CSS 类），持续约 6 秒后恢复默认状态。
目录结构
bash
复制代码
项目根目录/
│
├── index.html         # 主 HTML 文件
├── style.css          # 自定义 CSS 文件
├── 1blue.png          # 蓝发角色图片
├── 2red.png           # 红发角色图片
├── 3pink.png          # 粉发角色图片
├── 4yellow.png        # 金发角色图片
├── wallhaven-jxeelw_2560x1920.png  # 滚动视差背景图片 1
├── wallhaven-o559j7_2560x1920.png  # 滚动视差背景图片 2
├── wallhaven-1pvr23.png            # 滚动视差背景图片 3
└── wallhaven-3l69q3.jpg            # 滚动视差背景图片 4
使用说明
1. 克隆项目
bash
复制代码
git clone https://github.com/<你的用户名>/<仓库名>.git
2. 打开网页
直接使用浏览器打开 index.html 文件即可预览项目效果。

项目依赖
HTML5: 用于页面内容结构化。
CSS3: 用于页面样式设计，包括滚动视差效果。
JavaScript: 提供动态交互功能，例如标题悬停特效。
关键代码解析
1. 滚动视差实现
使用 CSS 背景固定效果实现：

css
复制代码
.parallax {
    background: url('./背景图片路径') no-repeat center center fixed;
    background-size: cover;
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
}
2. 动态标题特效
通过 JavaScript 添加和移除 CSS 类实现：

javascript
复制代码
const title = document.getElementById('title');
let hovered = false;

title.addEventListener('mouseover', () => {
    if (!hovered) {
        hovered = true;
        title.classList.add('hovered');
    }
    setTimeout(() => {
        hovered = false;
        title.classList.remove('hovered');
    }, 6000);
});
截图展示
角色展示

滚动视差背景

后续改进
增加更多角色卡片和信息。
提供多语言支持（如中文、英文）。
进一步优化滚动视差效果以支持移动设备。
许可证
该项目遵循 MIT 许可证，详情请查看 LICENSE。

作者
开发者: satalai
联系: your_email@example.com
GitHub: satalai
欢迎提交问题和建议！ 😊
