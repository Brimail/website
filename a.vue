<!-- The exported code uses Tailwind CSS. Install Tailwind CSS in your dev environment to ensure all styles work. -->
<template>
<div class="min-h-[1024px] bg-gradient-to-b from-gray-50 to-white relative">
<div class="absolute inset-0 overflow-hidden pointer-events-none">
<div class="moving-dots"></div>
</div>
<!-- 导航栏 -->
<nav class="fixed top-0 left-0 right-0 z-50 bg-white/95 backdrop-blur-sm border-b border-gray-100 h-16">
<div class="max-w-7xl mx-auto px-6 h-full flex items-center justify-between">
<div class="flex items-center space-x-2">
<el-icon class="text-2xl text-blue-600"><Message /></el-icon>
<span class="text-xl font-medium">简邮 Brimail</span>
</div>
<div class="flex items-center space-x-8">
<a v-for="(item, index) in navItems"
:key="index"
:class="{
  'text-gray-600 hover:text-blue-600 transition-colors cursor-pointer': true,
  'text-blue-600': activeNav === index
}"
@click="handleNavClick(index)">
{{ item }}
</a>
<button class="bg-blue-600 text-white px-6 py-2 !rounded-button cursor-pointer hover:bg-blue-700 transition-colors whitespace-nowrap">
立即下载
</button>
</div>
</div>
</nav>
<!-- Hero区域 -->
<div class="pt-16 relative overflow-hidden">
<div class="absolute inset-0 bg-cover bg-center" :style="{
backgroundImage: `url('https://public.readdy.ai/ai/img_res/8cec2894aba9d20cba0b2e9136abf84f.jpg')`
}"></div>
<div class="relative max-w-7xl mx-auto px-6 pt-20 pb-32">
<div class="max-w-2xl">
<h1 class="text-5xl font-bold text-gray-900 mb-6">
全平台智能邮件管理专家
</h1>
<p class="text-xl text-gray-600 mb-8">
简邮，让邮件管理变得简单高效。随时随地，畅享智能邮件体验。
</p>
<div class="flex space-x-4">
<button class="bg-blue-600 text-white px-8 py-3 !rounded-button text-lg cursor-pointer hover:bg-blue-700 transition-colors whitespace-nowrap">
免费试用
</button>
<button class="bg-white text-blue-600 px-8 py-3 !rounded-button text-lg border-2 border-blue-600 cursor-pointer hover:bg-blue-50 transition-colors whitespace-nowrap">
了解更多
</button>
</div>
</div>
</div>
</div>
<!-- 多端支持 -->
<div class="max-w-7xl mx-auto px-6 py-24">
<h2 class="text-3xl font-bold text-center mb-16">全平台支持，随时随地收发邮件</h2>
<div class="grid grid-cols-4 gap-8" style="perspective: 1000px;">
<div v-for="(platform, index) in platforms"
:key="index"
class="bg-white rounded-xl p-6 shadow-lg hover:shadow-xl transition-all duration-300 hover:-translate-y-2 hover:scale-105"
:style="{ '--animation-order': index }">
<div class="h-48 mb-6 overflow-hidden rounded-lg">
<img :src="platform.image" class="w-full h-full object-cover object-top" />
</div>
<h3 class="text-xl font-bold mb-4">{{ platform.name }}</h3>
<p class="text-gray-600 mb-4">{{ platform.description }}</p>
<button class="w-full bg-gray-50 text-blue-600 py-2 !rounded-button cursor-pointer hover:bg-gray-100 transition-colors whitespace-nowrap">
{{ platform.action }}
</button>
</div>
</div>
</div>
<!-- 功能特性 -->
<div class="bg-gray-50 py-24">
<div class="max-w-7xl mx-auto px-6">
<h2 class="text-3xl font-bold text-center mb-16">强大功能，智能体验</h2>
<div class="grid grid-cols-3 gap-8" style="perspective: 1000px;">
<div v-for="(feature, index) in features"
:key="index"
class="bg-white rounded-xl p-8 shadow hover:shadow-lg transition-all duration-300 hover:-translate-y-2 hover:scale-105 relative overflow-hidden"
:style="{ '--animation-order': index }">
<div class="absolute inset-0 bg-gradient-to-br from-transparent to-blue-50 opacity-0 hover:opacity-100 transition-opacity duration-300"></div>
<div class="relative z-10">
<el-icon class="text-3xl text-blue-600 mb-4 transform transition-transform group-hover:scale-110"><component :is="feature.icon" /></el-icon>
<h3 class="text-xl font-bold mb-4">{{ feature.title }}</h3>
<p class="text-gray-600">{{ feature.description }}</p>
</div>
<el-icon class="text-3xl text-blue-600 mb-4"><component :is="feature.icon" /></el-icon>
<h3 class="text-xl font-bold mb-4">{{ feature.title }}</h3>
<p class="text-gray-600">{{ feature.description }}</p>
</div>
</div>
</div>
</div>
<!-- 下载区域 -->
<div class="max-w-7xl mx-auto px-6 py-24">
<h2 class="text-3xl font-bold text-center mb-16">选择您的设备，开始体验</h2>
<div class="grid grid-cols-4 gap-6">
<div v-for="(download, index) in downloads"
:key="index"
class="bg-white border border-gray-200 rounded-xl p-6 text-center hover:border-blue-600 transition-colors">
<el-icon class="text-4xl text-gray-600 mb-4"><component :is="download.icon" /></el-icon>
<h3 class="text-lg font-bold mb-2">{{ download.name }}</h3>
<p class="text-sm text-gray-500 mb-4">{{ download.size }}</p>
<button class="w-full bg-blue-600 text-white py-2 !rounded-button cursor-pointer hover:bg-blue-700 transition-colors whitespace-nowrap">
立即下载
</button>
</div>
</div>
</div>
<!-- 页脚 -->
<footer class="bg-gray-900 text-white py-16">
<div class="max-w-7xl mx-auto px-6">
<div class="grid grid-cols-4 gap-8" style="perspective: 1000px;">
<div>
<div class="flex items-center space-x-2 mb-6">
<el-icon class="text-2xl text-blue-400"><Message /></el-icon>
<span class="text-xl font-medium">简邮 Brimail</span>
</div>
<p class="text-gray-400">智能邮件管理专家，让沟通更简单</p>
</div>
<div v-for="(section, index) in footerSections" :key="index">
<h4 class="font-bold mb-4">{{ section.title }}</h4>
<ul class="space-y-2">
<li v-for="(link, linkIndex) in section.links"
:key="linkIndex"
class="text-gray-400 hover:text-white cursor-pointer">
{{ link }}
</li>
</ul>
</div>
</div>
<div class="border-t border-gray-800 mt-12 pt-8 text-center text-gray-400">
<p>© 2025 简邮 Brimail. 保留所有权利</p>
</div>
</div>
</footer>
</div>
</template>
<script lang="ts" setup>
import { ref, onMounted, onUnmounted } from 'vue';
import { Message, Monitor, Iphone, Platform, Connection, Lock, Bell } from '@element-plus/icons-vue';

// 监听滚动事件来更新当前激活的导航项
const updateActiveNav = () => {
  const sections = [
    0, // 主页（顶部）
    document.querySelector('.bg-gray-50')?.offsetTop, // 功能特点
    document.querySelector('.max-w-7xl:nth-of-type(3)')?.offsetTop, // 全平台下载
    document.querySelector('footer')?.offsetTop // 技术支持
  ];
  
  const scrollPosition = window.scrollY + 100; // 添加偏移量以提前触发
  
  for (let i = sections.length - 1; i >= 0; i--) {
    if (sections[i] && scrollPosition >= sections[i]) {
      activeNav.value = i;
      break;
    }
  }
};

onMounted(() => {
  window.addEventListener('scroll', updateActiveNav);
});

onUnmounted(() => {
  window.removeEventListener('scroll', updateActiveNav);
});
import { ref } from 'vue';
const navItems = ['主页', '功能特点', '全平台下载', '技术支持'];
const activeNav = ref(0);

const handleNavClick = (index: number) => {
  activeNav.value = index;
  if (index === 0) {
    window.scrollTo({
      top: 0,
      behavior: 'smooth'
    });
  } else {
    // 根据索引滚动到对应的区域
    const sections = [
      null, // 主页不需要滚动目标
      document.querySelector('.bg-gray-50'), // 功能特点
      document.querySelector('.max-w-7xl:nth-of-type(3)'), // 全平台下载
      document.querySelector('footer') // 技术支持
    ];
    if (sections[index]) {
      sections[index]?.scrollIntoView({ behavior: 'smooth' });
    }
  }
};
const platforms = [
{
name: '桌面客户端',
description: '支持 Windows、macOS 和 Linux，享受完整邮件管理体验',
action: '下载客户端',
image: 'https://public.readdy.ai/ai/img_res/11186e6b3e6542501569a33d9bd09553.jpg'
},
{
name: '移动应用',
description: '随时随地查收邮件，支持 iOS 和 Android 系统',
action: '获取应用',
image: 'https://public.readdy.ai/ai/img_res/b6bd4af946314878819a9bf48f15eb29.jpg'
},
{
name: '平板应用',
description: '针对平板优化的界面，支持手写笔输入',
action: '下载应用',
image: 'https://public.readdy.ai/ai/img_res/9f79b6e34f9fc276a10df9fb5390b7f0.jpg'
},
{
name: 'Web 版本',
description: '无需下载安装，随时通过浏览器访问',
action: '立即使用',
image: 'https://public.readdy.ai/ai/img_res/a61cdb25ef7bb07072e8e7253ec112e8.jpg'
}
];
const features = [
{
icon: 'Connection',
title: '全平台数据同步',
description: '所有设备实时同步，邮件状态和设置无缝衔接'
},
{
icon: 'Lock',
title: '安全加密保护',
description: '全程 SSL 加密，确保您的邮件数据安全'
},
{
icon: 'Bell',
title: '智能通知提醒',
description: '重要邮件智能提醒，永不错过关键信息'
}
];
const downloads = [
{
icon: 'Monitor',
name: 'Windows 版',
size: '67.8 MB'
},
{
icon: 'Monitor',
name: 'macOS 版',
size: '72.3 MB'
},
{
icon: 'Iphone',
name: 'iOS 版',
size: '45.6 MB'
},
{
icon: 'Platform',
name: 'Android 版',
size: '38.9 MB'
}
];
const footerSections = [
{
title: '产品',
links: ['功能介绍', '更新日志', '开发计划', '价格方案']
},
{
title: '支持',
links: ['帮助中心', '视频教程', '常见问题', '联系我们']
},
{
title: '关于',
links: ['公司介绍', '团队博客', '加入我们', '隐私政策']
}
];
</script>
<style scoped>
.hero-gradient {
background: linear-gradient(135deg, rgba(59, 130, 246, 0.1) 0%, rgba(59, 130, 246, 0.05) 100%);
}
@keyframes float {
0% { transform: translateY(0); }
50% { transform: translateY(-10px); }
100% { transform: translateY(0); }
}
.moving-dots {
position: absolute;
top: 0;
left: 0;
width: 100%;
height: 100%;
background-image: radial-gradient(rgba(59, 130, 246, 0.1) 1px, transparent 1px);
background-size: 50px 50px;
animation: moveBackground 15s linear infinite;
opacity: 0.5;
}
@keyframes moveBackground {
0% {
background-position: 0 0;
}
100% {
background-position: 50px 50px;
}
}
.grid > div {
animation: float 6s ease-in-out infinite;
animation-delay: calc(var(--animation-order, 0) * 0.7s);
}
</style>
