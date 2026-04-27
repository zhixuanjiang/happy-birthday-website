# 多圆环粒子动画 / Multi-Ring Particle Animation

- 一个基于 Three.js 的 3D 粒子动画，包含旋转圆环、动态粒子云和生日快乐文字。  
- A 3D particle animation built with Three.js, featuring rotating rings, dynamic particle clouds, and a "Happy Birthday" text.

## 在线预览 / Live Demo

- 将你的 `happybirthday.html` 部署到任意静态服务器即可查看。  
- Deploy the `happybirthday.html` to any static server to view.

## 功能特点 / Features

- 粒子系统包含 **约 50 万粒子**，形成多个圆环与爱心形状  
- 粒子颜色在 **橙黄至蓝紫** 之间渐变，并随时间微动  
- 每个粒子独立运动，形成流动的“呼吸”效果  
- 轨道控制：鼠标拖拽旋转视角，右键平移，滚轮缩放  
- 3D 半透文字：“Happy Birthday”  
- 丰富粒子叠加，视觉上类似星云或烟花绽放  

---

- Particle system with **~500k particles** forming rings and a heart shape  
- Color gradient from **orange-yellow to blue-purple** with subtle motion over time  
- Each particle moves independently, creating a flowing “breathing” effect  
- Orbit controls: drag to rotate, right-click to pan, scroll to zoom  
- 3D semi‑transparent text: “Happy Birthday”  
- Dense particle overlap, visually similar to a nebula or fireworks

## 技术栈 / Tech Stack

- [Three.js r136](https://threejs.org/) – WebGL 渲染引擎  
- JavaScript (ES Module) – 所有逻辑内嵌于 HTML 中  
- OrbitControls – 相机交互  
- FontLoader + TextGeometry – 3D 文字生成

## 文件结构 / File Structure
your-project/
├── happybirthday.html # 完整代码（包含样式、脚本）
└── README.md # 项目说明

> 无需额外依赖，直接打开 `happybirthday.html` 即可运行。  
> No extra dependencies – just open `happybirthday.html` in a browser.

## 运行方式 / How to Run

1. 下载 `happybirthday.html` 到本地  
2. 双击用现代浏览器（Chrome / Edge / Firefox）打开  
3. 等待字体和模型加载（约 2‑3 秒）  
4. 鼠标拖拽旋转视角，滚动缩放  

---

1. Download `happybirthday.html` to your computer  
2. Double‑click to open with a modern browser (Chrome / Edge / Firefox)  
3. Wait ~2‑3 seconds for font and model loading  
4. Drag to rotate, scroll to zoom

## 自定义修改 / Customization

| 修改项 / What to change | 位置 / Where | 说明 / Note |
|------------------------|--------------|--------------|
| 文字内容 | `TextGeometry('Happy Birthday')` | 改为你想要的中文或英文 |
| 文字颜色/透明度 | `color: 0xd06090` / `opacity: 0.5` | RGB 十六进制，opacity 范围 0‑1 |
| 粒子数量 | `new Array(100000)` / `createHeartPoints(200000)` | 增加/减少数值（注意性能） |
| 动画速度 | `t * 0.3` / `t * 1` 等系数 | 系数越大旋转越快 |
| 背景颜色 | `scene.background = new THREE.Color(0x160016)` | 任意十六进制颜色 |

## 性能提示 / Performance Notes

- 总粒子数约 **50 万**，在集成显卡上可能略卡，可适当减少数量  
- 推荐使用独立显卡或 Chrome 浏览器  
- 移动设备上建议降至 **10 万粒子** 以内

---

- Total particles: **~500k** – may be heavy on integrated GPUs; reduce the count if needed  
- Dedicated GPU or Chrome browser recommended  
- On mobile, keep particle count **below 100k**

## 灵感与原项目 / Inspiration & Original Credit

本项目原始风格与部分算法参考了网络上的"粒子星辰"演示。因时间久远，原始出处已不可考。

The original style and some algorithms of this project reference an online "Particle Starfield" demo. Due to the passage of time, the original source can no longer be traced.