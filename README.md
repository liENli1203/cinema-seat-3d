# 🎬 3D 电影院选座视角模拟器 (3D Cinema Seat Previewer)

<p align="center">
  <img src="https://img.shields.io/badge/Three.js-WebGL-000000?style=flat-square&logo=three.js" alt="Three.js" />
  <img src="https://img.shields.io/badge/Architecture-Single%20HTML-E34F26?style=flat-square&logo=html5&logoColor=white" alt="Single HTML" />
  <img src="https://img.shields.io/badge/UI-Desktop%20%7C%20Mobile%20Portrait%20%26%20Landscape-2563EB?style=flat-square" alt="Responsive UI" />
  <img src="https://img.shields.io/badge/License-MIT-10B981?style=flat-square" alt="MIT License" />
</p>

一款基于 **Three.js** 构建的纯前端、零构建、单文件 **3D 影院选座视角模拟器**。在购票前即可沉浸式预览不同影厅、不同排号与座位的真实银幕视野、前排遮挡情况以及专业光学观影评分。

> 🌐 **在线体验地址**：[https://你的用户名.github.io/cinema-seat-3d/](https://你的用户名.github.io/cinema-seat-3d/)

---

## 📸 效果预览

<!-- 上线后可将桌面端与手机横竖屏截图放入 assets 文件夹，取消下方注释即可展示 -->
<!--
| 桌面端第一人称视角 | 手机竖屏选座 | 手机横屏沉浸模式 |
| :---: | :---: | :---: |
| ![桌面端](./assets/desktop.png) | ![手机竖屏](./assets/mobile-portrait.png) | ![手机横屏](./assets/mobile-landscape.png) |
-->

---

## ✨ 核心功能亮点

- **🏛️ 四种真实影厅规格**：一键切换 **标准厅**、**IMAX 巨幕厅**（微曲面高银幕 + 陡峭阶梯）、**杜比影院**（暗黑吸音空间 + 蓝光氛围灯带）与 **小型 VIP 厅**，切换后自动定位当前影厅黄金 C 位。
- **👁️ 第一人称 & 3D 全景双视角**：
  - **第一人称视角**：支持鼠标/触屏自由转头环顾，提供 **120cm~190cm 观众身高调节**、**模拟前排观众遮挡** 以及 **放映暗场 / 入场照明** 切换。
  - **3D 全景视角**：360° 旋转缩放俯瞰影厅（高角度自动隐藏天花板防遮挡），支持在 3D 场景中直接点击选座、双击入座。
- **🎞️ 动态银幕测试与自定义投屏**：内置 **星际大片动态预览**（含宽银幕遮幅与双语字幕）、**THX 视角校准网格**，并支持上传本地图片实时投屏到 3D 银幕。
- **📊 科学光学观影评测**：按真实 3D 物理空间坐标实时计算 **综合评分（0~100 / S+~C 等级）**、**水平视角（HFOV）**、**中心/顶部仰角**、**水平偏心角** 与 **视距比**。
- **📱 全端三态响应式适配**：独立适配 **桌面宽屏**、**手机竖屏（底部悬浮栏 + 底部抽屉 + 视野自动上移）** 与 **手机横屏（右侧垂直栏 + 右侧滑出抽屉 + 视野自动左移 + 超宽屏 FOV 防畸变校准）**，支持安全区避让与纯享观影模式。
- **🛡️ 高可用防错与一键刷新**：内置 **jsDelivr → UNPKG → cdnjs** 多源 CDN 自动降级、8 秒加载超时保护、WebGL 上下文丢失自愈，以及顶部高亮「刷新」按钮实现不丢状态的就地重建。

---

## 🎮 操作指南

| 场景 / 设备 | 操作方式 | 功能说明 |
| :--- | :--- | :--- |
| **第一人称视角** | 鼠标拖拽 / 单指滑动 | 自由转动头部观察银幕与周边环境 |
| **3D 全景视角** | 拖拽旋转 / 滚轮或双指缩放 | 俯瞰影厅布局，单击选座、双击直接入座 |
| **桌面快捷键** | `↑` `↓` `←` `→` 方向键 | 快速切换前后左右相邻座位 |
| **桌面快捷键** | `R` 键 | 一键将头部视角居中回正对准银幕 |
| **异常处理** | 点击顶部「刷新」按钮 | 保留当前影厅与座位，就地重建 3D 渲染场景 |

---

## 🚀 本地运行与部署

本项目为**纯前端单文件架构**，无需安装 Node.js 或任何构建工具：

1. 克隆或下载仓库到本地：
   ```bash
   git clone [https://github.com/你的用户名/cinema-seat-3d.git](https://github.com/你的用户名/cinema-seat-3d.git)
   ```
2. 直接使用现代浏览器（Chrome / Edge / Safari / Firefox）双击打开 `index.html` 即可运行。
3. 如需二次部署，只需将 `index.html` 推送至 GitHub 仓库并开启 **GitHub Pages**，或直接导入 **Cloudflare Pages / Vercel**。

---

## 🛠️ 技术栈

- **3D 渲染引擎**：[Three.js](https://threejs.org/)（WebGL + Canvas 动态纹理）
- **交互与布局**：原生 HTML5 / CSS3（`100dvh`、`env(safe-area-inset-*)` 三态媒体查询）+ Vanilla JavaScript

---

## 📄 开源协议

本项目基于 [MIT License](LICENSE) 开源，欢迎 Fork、Star 或提交 Issue 提出改进建议。