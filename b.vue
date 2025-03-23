<!-- The exported code uses Tailwind CSS. Install Tailwind CSS in your dev environment to ensure all styles work. -->

<template>
  <div class="min-h-screen bg-white">
    <!-- 导航栏 -->
    <nav class="fixed top-0 w-full bg-white/95 backdrop-blur-sm z-50 border-b border-gray-100">
      <div class="max-w-7xl mx-auto px-4 h-16 flex items-center justify-between">
        <div class="flex items-center space-x-2">
          <el-icon class="text-blue-600 text-2xl"><Message /></el-icon>
          <span class="text-xl font-semibold">Brimail 简邮</span>
        </div>
        
        <div class="flex items-center space-x-8">
          <a href="#features" class="text-gray-600 hover:text-blue-600 cursor-pointer">产品特性</a>
          <a href="#pricing" class="text-gray-600 hover:text-blue-600 cursor-pointer">价格方案</a>
          <a href="#help" class="text-gray-600 hover:text-blue-600 cursor-pointer">帮助中心</a>
          <a href="#download" class="text-gray-600 hover:text-blue-600 cursor-pointer">下载客户端</a>
          <button class="!rounded-button px-6 py-2 bg-blue-600 text-white hover:bg-blue-700 cursor-pointer whitespace-nowrap">登录 / 注册</button>
        </div>
      </div>
    </nav>

    <!-- Hero区域 -->
    <div class="pt-16 relative overflow-hidden">
      <div class="max-w-7xl mx-auto px-4 py-20 flex items-center">
        <div class="w-1/2 pr-8">
          <h1 class="text-5xl font-bold leading-tight mb-6">让邮件处理更简单、更高效</h1>
          <p class="text-xl text-gray-600 mb-8">专为现代办公设计的智能邮件客户端，让您的工作效率提升 200%</p>
          <button class="!rounded-button px-8 py-4 bg-blue-600 text-white text-lg hover:bg-blue-700 cursor-pointer whitespace-nowrap">立即免费体验</button>
        </div>
        <div class="w-1/2">
          <img :src="heroImage" class="w-full h-[400px] object-cover object-top rounded-lg shadow-2xl" alt="邮件客户端界面" />
        </div>
      </div>
    </div>

    <!-- 核心功能 -->
    <div class="py-20 bg-gray-50">
      <div class="max-w-7xl mx-auto px-4">
        <h2 class="text-3xl font-bold text-center mb-16">为什么选择 Brimail 简邮？</h2>
        <div class="grid grid-cols-3 gap-8">
          <div v-for="(feature, index) in features" :key="index" class="bg-white p-8 rounded-xl shadow-sm hover:shadow-lg transition-shadow">
            <img :src="feature.image" class="w-full h-48 object-cover object-top rounded-lg mb-6" alt="feature" />
            <h3 class="text-xl font-semibold mb-4">{{ feature.title }}</h3>
            <p class="text-gray-600">{{ feature.description }}</p>
          </div>
        </div>
      </div>
    </div>

    <!-- 数据对比 -->
    <div class="py-20">
      <div class="max-w-7xl mx-auto px-4">
        <h2 class="text-3xl font-bold text-center mb-16">性能对比</h2>
        <div ref="chartRef" class="w-full h-[400px]"></div>
      </div>
    </div>

    <!-- 用户评价 -->
    <div class="py-20 bg-gray-50">
      <div class="max-w-7xl mx-auto px-4">
        <h2 class="text-3xl font-bold text-center mb-16">用户评价</h2>
        <swiper 
          :modules="swiperModules"
          :slides-per-view="3"
          :space-between="30"
          :autoplay="{ delay: 3000 }"
          :pagination="{ clickable: true }"
          class="testimonials-swiper"
        >
          <swiper-slide v-for="(testimonial, index) in testimonials" :key="index">
            <div class="bg-white p-6 rounded-xl shadow-sm">
              <div class="flex items-center mb-4">
                <img :src="testimonial.avatar" class="w-12 h-12 rounded-full object-cover" :alt="testimonial.name" />
                <div class="ml-4">
                  <h4 class="font-semibold">{{ testimonial.name }}</h4>
                  <p class="text-sm text-gray-600">{{ testimonial.position }}</p>
                </div>
              </div>
              <p class="text-gray-600">{{ testimonial.content }}</p>
            </div>
          </swiper-slide>
        </swiper>
      </div>
    </div>

    <!-- 价格方案 -->
    <div class="py-20">
      <div class="max-w-7xl mx-auto px-4">
        <h2 class="text-3xl font-bold text-center mb-16">价格方案</h2>
        <div class="grid grid-cols-3 gap-8">
          <div v-for="(plan, index) in plans" :key="index" 
               class="bg-white p-8 rounded-xl shadow-sm hover:shadow-lg transition-shadow border border-gray-100">
            <h3 class="text-2xl font-bold mb-4">{{ plan.name }}</h3>
            <div class="text-3xl font-bold mb-6">
              <span class="text-lg">￥</span>{{ plan.price }}
              <span class="text-base font-normal text-gray-600">/月</span>
            </div>
            <ul class="space-y-4 mb-8">
              <li v-for="(feature, fIndex) in plan.features" :key="fIndex" class="flex items-center">
                <el-icon class="text-green-500 mr-2"><Check /></el-icon>
                <span>{{ feature }}</span>
              </li>
            </ul>
            <button class="!rounded-button w-full py-3 text-center cursor-pointer whitespace-nowrap"
                    :class="index === 1 ? 'bg-blue-600 text-white hover:bg-blue-700' : 'border border-blue-600 text-blue-600 hover:bg-blue-50'">
              立即选购
            </button>
          </div>
        </div>
      </div>
    </div>

    <!-- 底部 -->
    <footer class="bg-gray-900 text-gray-300 py-16">
      <div class="max-w-7xl mx-auto px-4 grid grid-cols-4 gap-8">
        <div>
          <h4 class="text-white font-semibold mb-4">产品</h4>
          <ul class="space-y-2">
            <li><a href="#" class="hover:text-white cursor-pointer">产品特性</a></li>
            <li><a href="#" class="hover:text-white cursor-pointer">价格方案</a></li>
            <li><a href="#" class="hover:text-white cursor-pointer">下载客户端</a></li>
            <li><a href="#" class="hover:text-white cursor-pointer">更新日志</a></li>
          </ul>
        </div>
        <div>
          <h4 class="text-white font-semibold mb-4">资源</h4>
          <ul class="space-y-2">
            <li><a href="#" class="hover:text-white cursor-pointer">帮助文档</a></li>
            <li><a href="#" class="hover:text-white cursor-pointer">开发者文档</a></li>
            <li><a href="#" class="hover:text-white cursor-pointer">API 接口</a></li>
            <li><a href="#" class="hover:text-white cursor-pointer">技术支持</a></li>
          </ul>
        </div>
        <div>
          <h4 class="text-white font-semibold mb-4">关于我们</h4>
          <ul class="space-y-2">
            <li><a href="#" class="hover:text-white cursor-pointer">公司介绍</a></li>
            <li><a href="#" class="hover:text-white cursor-pointer">加入我们</a></li>
            <li><a href="#" class="hover:text-white cursor-pointer">联系方式</a></li>
            <li><a href="#" class="hover:text-white cursor-pointer">新闻动态</a></li>
          </ul>
        </div>
        <div>
          <h4 class="text-white font-semibold mb-4">联系我们</h4>
          <p class="mb-4">商务合作：business@brimail.com</p>
          <p>技术支持：support@brimail.com</p>
          <div class="flex space-x-4 mt-4">
            <el-icon class="text-xl cursor-pointer"><Position /></el-icon>
            <el-icon class="text-xl cursor-pointer"><Message /></el-icon>
            <el-icon class="text-xl cursor-pointer"><ChatDotRound /></el-icon>
          </div>
        </div>
      </div>
      <div class="max-w-7xl mx-auto px-4 mt-16 pt-8 border-t border-gray-800">
        <p class="text-center">© 2025 Brimail 简邮. 保留所有权利</p>
      </div>
    </footer>
  </div>
</template>

<script lang="ts" setup>
import { ref, onMounted } from 'vue';
import { Swiper, SwiperSlide } from 'swiper/vue';
import { Pagination, Autoplay } from 'swiper/modules';
import * as echarts from 'echarts';
import { Message, Check, Position, ChatDotRound } from '@element-plus/icons-vue';

const swiperModules = [Pagination, Autoplay];
const chartRef = ref<HTMLElement>();

const heroImage = 'https://public.readdy.ai/ai/img_res/eae71b3c0a893ee5ae15b81bb1cb43c8.jpg';

const features = [
  {
    title: '智能分类',
    description: '基于 AI 的邮件智能分类系统，自动识别重要邮件，让您的收件箱井然有序',
    image: 'https://public.readdy.ai/ai/img_res/ce75e5d8edbbf39a57f0de1a9e7b2a56.jpg'
  },
  {
    title: '快速回复',
    description: '内置智能回复模板，一键生成专业邮件回复，节省 80% 写作时间',
    image: 'https://public.readdy.ai/ai/img_res/d2135c3c2b720204062a6131a84e7d7e.jpg'
  },
  {
    title: '安全防护',
    description: '军工级加密技术，内置防钓鱼系统，让您的邮件安全无忧',
    image: 'https://public.readdy.ai/ai/img_res/8b82cecfea7f08f68e285dda602aadf7.jpg'
  }
];

const testimonials = [
  {
    name: '陈思远',
    position: '科技公司 CEO',
    content: 'Brimail 简邮让我的邮件处理效率提升了 3 倍，智能分类功能特别好用，强烈推荐！',
    avatar: 'https://public.readdy.ai/ai/img_res/8be2e7e1344f2fa8b0a474981fc17977.jpg'
  },
  {
    name: '林雨晴',
    position: '营销总监',
    content: '作为营销人员，每天要处理大量邮件，有了 Brimail 简邮，工作效率提升很多。',
    avatar: 'https://public.readdy.ai/ai/img_res/46316bb5ac5ab06aea9e58bc1ad3293e.jpg'
  },
  {
    name: '张明宇',
    position: '创业者',
    content: '界面简洁，功能强大，是我见过最好用的邮件客户端，值得推荐给每一个人。',
    avatar: 'https://public.readdy.ai/ai/img_res/2147f6a1eba67eeee9094bc61ed33988.jpg'
  }
];

const plans = [
  {
    name: '个人免费版',
    price: '0',
    features: [
      '基础邮件管理',
      '智能分类',
      '5GB 存储空间',
      '基础客户端支持'
    ]
  },
  {
    name: '专业版',
    price: '29',
    features: [
      '所有免费版功能',
      '无限存储空间',
      'AI 智能回复',
      '优先客服支持',
      '多设备同步'
    ]
  },
  {
    name: '企业版',
    price: '99',
    features: [
      '所有专业版功能',
      '企业级安全防护',
      '专属技术支持',
      '自定义域名',
      '团队协作功能'
    ]
  }
];

onMounted(() => {
  const chart = echarts.init(chartRef.value as HTMLElement);
  const option = {
    animation: false,
    tooltip: {
      trigger: 'axis',
      axisPointer: {
        type: 'shadow'
      }
    },
    legend: {
      data: ['Brimail 简邮', '其他邮件客户端']
    },
    grid: {
      left: '3%',
      right: '4%',
      bottom: '3%',
      containLabel: true
    },
    xAxis: {
      type: 'value',
      boundaryGap: [0, 0.01]
    },
    yAxis: {
      type: 'category',
      data: ['响应速度', '垃圾邮件过滤', '智能分类准确率', '用户满意度']
    },
    series: [
      {
        name: 'Brimail 简邮',
        type: 'bar',
        data: [98, 95, 93, 96],
        itemStyle: {
          color: '#2563eb'
        }
      },
      {
        name: '其他邮件客户端',
        type: 'bar',
        data: [85, 82, 80, 85],
        itemStyle: {
          color: '#93c5fd'
        }
      }
    ]
  };
  chart.setOption(option);

  window.addEventListener('resize', () => {
    chart.resize();
  });
});
</script>

<style scoped>
.testimonials-swiper {
  padding-bottom: 50px !important;
}

.testimonials-swiper :deep(.swiper-pagination-bullet) {
  width: 10px;
  height: 10px;
  background: #93c5fd;
  opacity: 0.5;
}

.testimonials-swiper :deep(.swiper-pagination-bullet-active) {
  background: #2563eb;
  opacity: 1;
}
</style>

