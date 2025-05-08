<!-- The exported code uses Tailwind CSS. Install Tailwind CSS in your dev environment to ensure all styles work. -->
<template>
  <div class="min-h-screen bg-white">
    <!-- 导航栏 -->
    <header
      class="fixed top-0 left-0 right-0 bg-gradient-to-r from-blue-900 to-blue-800 shadow-md z-50"
    >
      <div
        class="container mx-auto px-6 py-3 flex items-center justify-between"
      >
        <div class="flex items-center">
          <div class="text-white font-bold text-2xl flex items-center">
            <el-icon class="mr-2 text-3xl"><Message /></el-icon>
            <span>Brimail</span>
          </div>
        </div>
        <nav class="hidden md:flex items-center space-x-8">
          <a
            href="#"
            class="text-white hover:text-yellow-300 font-medium whitespace-nowrap cursor-pointer"
            >首页</a
          >
          <a
            href="#"
            class="text-white hover:text-yellow-300 font-medium whitespace-nowrap cursor-pointer"
            >产品服务</a
          >
          <a
            href="#"
            class="text-white hover:text-yellow-300 font-medium whitespace-nowrap cursor-pointer"
            >国际互联</a
          >
          <a
            href="#"
            class="text-white hover:text-yellow-300 font-medium whitespace-nowrap cursor-pointer"
            >安全保障</a
          >
          <a
            href="#"
            class="text-white hover:text-yellow-300 font-medium whitespace-nowrap cursor-pointer"
            >成功案例</a
          >
          <a
            href="#"
            class="text-white hover:text-yellow-300 font-medium whitespace-nowrap cursor-pointer"
            >关于我们</a
          >
        </nav>
        <div class="flex items-center space-x-4">
          <div
            class="flex items-center border border-blue-300 rounded-full px-3 py-1 text-white cursor-pointer"
          >
            <span>中文</span>
            <el-icon class="ml-1"><ArrowDown /></el-icon>
          </div>
          <button
            class="bg-yellow-500 hover:bg-yellow-600 text-blue-900 font-bold py-2 px-4 !rounded-button whitespace-nowrap cursor-pointer"
          >
            立即登录
          </button>
        </div>
        <div class="md:hidden">
          <el-icon class="text-white text-2xl cursor-pointer"><Menu /></el-icon>
        </div>
      </div>
    </header>
    <!-- Hero 区域 -->
    <section class="pt-24 relative overflow-hidden" style="min-height: 650px">
      <div class="absolute inset-0 z-0">
        <img
          src="https://readdy.ai/api/search-image?query=Abstract%20world%20map%20with%20glowing%20digital%20connections%2C%20blue%20gradient%20background%20with%20golden%20light%20paths%20representing%20the%20Belt%20and%20Road%20Initiative%2C%20modern%20tech%20aesthetic%20with%20flowing%20data%20streams%20and%20network%20nodes%2C%20elegant%20and%20professional%20design%20for%20global%20communication&width=1440&height=650&seq=hero-bg-1&orientation=landscape"
          alt="全球互联网络背景"
          class="w-full h-full object-cover object-top"
        />
      </div>
      <div
        class="container mx-auto px-6 py-20 relative z-10 flex flex-col md:flex-row items-center"
      >
        <div class="md:w-1/2 text-white">
          <h1 class="text-4xl md:text-5xl font-bold mb-4 leading-tight">
            Brimail — 搭建全球互联桥梁
          </h1>
          <p class="text-xl md:text-2xl mb-8 opacity-90">
            秉承 Bri 精神，开启无限沟通可能
          </p>
          <p class="text-lg mb-10 opacity-80 max-w-xl">
            连接东西方的专业邮件服务平台，为全球用户提供安全、高效、智能的跨境通信解决方案。
          </p>
          <div class="flex flex-wrap gap-4">
            <button
              class="bg-yellow-500 hover:bg-yellow-600 text-blue-900 font-bold py-3 px-8 !rounded-button whitespace-nowrap cursor-pointer"
            >
              立即注册
            </button>
            <button
              class="bg-transparent border-2 border-white hover:bg-white/10 text-white font-bold py-3 px-8 !rounded-button whitespace-nowrap cursor-pointer"
            >
              了解更多
            </button>
          </div>
        </div>
      </div>
      <div
        class="absolute bottom-5 left-1/2 transform -translate-x-1/2 text-white animate-bounce"
      >
        <el-icon class="text-3xl"><ArrowDown /></el-icon>
      </div>
    </section>
    <!-- 产品服务亮点 -->
    <section class="py-20 bg-gray-50">
      <div class="container mx-auto px-6">
        <div class="text-center mb-16">
          <h2 class="text-3xl font-bold text-blue-900 mb-4">
            全球化邮件服务平台
          </h2>
          <p class="text-gray-600 max-w-2xl mx-auto">
            Brimail
            提供专业的跨境通信解决方案，让您的邮件传递更加安全、高效、智能。
          </p>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
          <div
            class="bg-white rounded-xl shadow-lg p-8 transition-all duration-300 hover:shadow-xl hover:-translate-y-1 cursor-pointer"
          >
            <div
              class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6 mx-auto"
            >
              <el-icon class="text-blue-700 text-3xl"><Connection /></el-icon>
            </div>
            <h3 class="text-xl font-bold text-blue-900 mb-3 text-center">
              全球高效传输
            </h3>
            <p class="text-gray-600 text-center">
              借助先进的云技术确保邮件传递快速无误，全球范围内的通信无障碍。
            </p>
          </div>
          <div
            class="bg-white rounded-xl shadow-lg p-8 transition-all duration-300 hover:shadow-xl hover:-translate-y-1 cursor-pointer"
          >
            <div
              class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6 mx-auto"
            >
              <el-icon class="text-blue-700 text-3xl"><Lock /></el-icon>
            </div>
            <h3 class="text-xl font-bold text-blue-900 mb-3 text-center">
              国际级安全保障
            </h3>
            <p class="text-gray-600 text-center">
              提供端到端加密技术，符合各国数据隐私标准，保障您的通信安全。
            </p>
          </div>
          <div
            class="bg-white rounded-xl shadow-lg p-8 transition-all duration-300 hover:shadow-xl hover:-translate-y-1 cursor-pointer"
          >
            <div
              class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6 mx-auto"
            >
              <el-icon class="text-blue-700 text-3xl"><ChatDotRound /></el-icon>
            </div>
            <h3 class="text-xl font-bold text-blue-900 mb-3 text-center">
              跨境通信支持
            </h3>
            <p class="text-gray-600 text-center">
              内置多语言、全球服务器和数据备份功能，确保跨国通信无缝衔接。
            </p>
          </div>
          <div
            class="bg-white rounded-xl shadow-lg p-8 transition-all duration-300 hover:shadow-xl hover:-translate-y-1 cursor-pointer"
          >
            <div
              class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6 mx-auto"
            >
              <el-icon class="text-blue-700 text-3xl"><Files /></el-icon>
            </div>
            <h3 class="text-xl font-bold text-blue-900 mb-3 text-center">
              智能分类与检索
            </h3>
            <p class="text-gray-600 text-center">
              高效邮件管理系统，让用户随时轻松查找重要信息，提升工作效率。
            </p>
          </div>
        </div>
      </div>
    </section>
    <!-- 国际互联与合作展示 -->
    <section class="py-20 bg-white">
      <div class="container mx-auto px-6">
        <div class="text-center mb-16">
          <h2 class="text-3xl font-bold text-blue-900 mb-4">
            国际互联与全球合作
          </h2>
          <p class="text-gray-600 max-w-2xl mx-auto">
            Brimail
            在"一带一路"沿线建立战略节点和数据中心，打造全球化邮件服务网络。
          </p>
        </div>
        <div class="mb-16 relative h-96 rounded-xl overflow-hidden shadow-xl">
          <img
            src="https://readdy.ai/api/search-image?query=Digital%20world%20map%20with%20Asia%20on%20the%20left%20and%20Americas%20on%20the%20right%2C%20without%20country%20borders%2C%20featuring%20glowing%20connection%20lines%20between%20major%20cities%2C%20bright%20network%20nodes%20in%20blue%20and%20gold%20color%20scheme%2C%20modern%20data%20visualization%20showing%20global%20connectivity%20with%20Pacific%20Ocean%20centered&width=1200&height=600&seq=map-bg-2&orientation=landscape"
            alt="以太平洋为中心的全球互联网络地图"
            class="w-full h-full object-cover object-top"
          />
          <div
            class="absolute inset-0 bg-gradient-to-r from-blue-900/70 to-transparent flex items-center"
          >
            <div class="p-10 text-white max-w-lg">
              <h3 class="text-2xl font-bold mb-4">全球战略布局</h3>
              <p class="mb-6">
                Brimail 已在全球 35
                个国家和地区建立数据中心和服务节点，为用户提供低延迟、高可用的邮件服务。
              </p>
              <button
                class="bg-yellow-500 hover:bg-yellow-600 text-blue-900 font-bold py-2 px-6 !rounded-button whitespace-nowrap cursor-pointer"
              >
                查看详情
              </button>
            </div>
          </div>
        </div>
        <div class="mb-10">
          <h3 class="text-2xl font-bold text-blue-900 mb-8 text-center">
            合作伙伴
          </h3>
          <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-6 gap-8">
            <div
              class="flex flex-col items-center justify-center p-4 rounded-lg bg-gray-50"
            >
              <el-icon class="text-4xl text-gray-600 mb-2"><Apple /></el-icon>
              <span class="text-gray-700 font-medium">Apple Inc.</span>
            </div>
            <div
              class="flex flex-col items-center justify-center p-4 rounded-lg bg-gray-50"
            >
              <el-icon class="text-4xl text-gray-600 mb-2"><Aim /></el-icon>
              <span class="text-gray-700 font-medium">Target Corp</span>
            </div>
            <div
              class="flex flex-col items-center justify-center p-4 rounded-lg bg-gray-50"
            >
              <el-icon class="text-4xl text-gray-600 mb-2"><Cloudy /></el-icon>
              <span class="text-gray-700 font-medium">Cloud Tech</span>
            </div>
            <div
              class="flex flex-col items-center justify-center p-4 rounded-lg bg-gray-50"
            >
              <el-icon class="text-4xl text-gray-600 mb-2"
                ><DataAnalysis
              /></el-icon>
              <span class="text-gray-700 font-medium">Data Systems</span>
            </div>
            <div
              class="flex flex-col items-center justify-center p-4 rounded-lg bg-gray-50"
            >
              <el-icon class="text-4xl text-gray-600 mb-2"><Dish /></el-icon>
              <span class="text-gray-700 font-medium">Global Connect</span>
            </div>
            <div
              class="flex flex-col items-center justify-center p-4 rounded-lg bg-gray-50"
            >
              <el-icon class="text-4xl text-gray-600 mb-2"><Monitor /></el-icon>
              <span class="text-gray-700 font-medium">Tech Monitor</span>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- 安全、信任与数据保护 -->
    <section class="py-20 bg-gray-50">
      <div class="container mx-auto px-6">
        <div class="text-center mb-16">
          <h2 class="text-3xl font-bold text-blue-900 mb-4">
            安全、信任与数据保护
          </h2>
          <p class="text-gray-600 max-w-2xl mx-auto">
            Brimail 致力于为全球用户提供最高级别的安全保障和数据隐私保护。
          </p>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-16">
          <div class="bg-white rounded-xl shadow-md p-8">
            <div class="flex items-center mb-6">
              <div
                class="w-12 h-12 bg-blue-100 rounded-full flex items-center justify-center mr-4"
              >
                <el-icon class="text-blue-700 text-2xl"><Lock /></el-icon>
              </div>
              <h3 class="text-xl font-bold text-blue-900">端到端加密</h3>
            </div>
            <p class="text-gray-600">
              采用最先进的加密技术，确保您的邮件内容在传输和存储过程中不被未授权访问。
            </p>
          </div>
          <div class="bg-white rounded-xl shadow-md p-8">
            <div class="flex items-center mb-6">
              <div
                class="w-12 h-12 bg-blue-100 rounded-full flex items-center justify-center mr-4"
              >
                <el-icon class="text-blue-700 text-2xl"><Document /></el-icon>
              </div>
              <h3 class="text-xl font-bold text-blue-900">合规认证</h3>
            </div>
            <p class="text-gray-600">
              符合全球主要数据保护法规，包括 GDPR、CCPA
              等，保障您的数据合规使用。
            </p>
          </div>
          <div class="bg-white rounded-xl shadow-md p-8">
            <div class="flex items-center mb-6">
              <div
                class="w-12 h-12 bg-blue-100 rounded-full flex items-center justify-center mr-4"
              >
                <el-icon class="text-blue-700 text-2xl"><AlarmClock /></el-icon>
              </div>
              <h3 class="text-xl font-bold text-blue-900">7/24 监控</h3>
            </div>
            <p class="text-gray-600">
              全天候安全监控系统，实时检测和防御潜在威胁，保障服务稳定运行。
            </p>
          </div>
        </div>
        <!-- 用户反馈 -->
        <div class="bg-white rounded-xl shadow-lg p-8">
          <h3 class="text-2xl font-bold text-blue-900 mb-8 text-center">
            用户反馈
          </h3>
          <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
            <div class="p-6 bg-gray-50 rounded-lg">
              <div class="flex items-center mb-4">
                <img
                  src="https://readdy.ai/api/search-image?query=Professional%20Asian%20businessman%20portrait%2C%20confident%20smile%2C%20business%20attire%2C%20neutral%20background%2C%20corporate%20headshot%20style%2C%20high%20quality%20professional%20photo&width=100&height=100&seq=user1&orientation=squarish"
                  alt="用户头像"
                  class="w-12 h-12 rounded-full object-cover mr-4"
                />
                <div>
                  <h4 class="font-bold text-blue-900">李明</h4>
                  <p class="text-gray-500 text-sm">国际贸易公司 CEO</p>
                </div>
              </div>
              <p class="text-gray-600">
                "Brimail
                帮助我们解决了与海外客户沟通的难题，邮件传输速度快，安全性高，是我们业务拓展的得力助手。"
              </p>
            </div>
            <div class="p-6 bg-gray-50 rounded-lg">
              <div class="flex items-center mb-4">
                <img
                  src="https://readdy.ai/api/search-image?query=Professional%20European%20businesswoman%20portrait%2C%20confident%20smile%2C%20business%20attire%2C%20neutral%20background%2C%20corporate%20headshot%20style%2C%20high%20quality%20professional%20photo&width=100&height=100&seq=user2&orientation=squarish"
                  alt="用户头像"
                  class="w-12 h-12 rounded-full object-cover mr-4"
                />
                <div>
                  <h4 class="font-bold text-blue-900">Sarah Johnson</h4>
                  <p class="text-gray-500 text-sm">跨国企业 IT 总监</p>
                </div>
              </div>
              <p class="text-gray-600">
                "作为 IT 总监，我对 Brimail
                的安全性和稳定性非常满意。它帮助我们团队在全球范围内高效协作。"
              </p>
            </div>
            <div class="p-6 bg-gray-50 rounded-lg">
              <div class="flex items-center mb-4">
                <img
                  src="https://readdy.ai/api/search-image?query=Professional%20Middle%20Eastern%20businessman%20portrait%2C%20confident%20smile%2C%20business%20attire%2C%20neutral%20background%2C%20corporate%20headshot%20style%2C%20high%20quality%20professional%20photo&width=100&height=100&seq=user3&orientation=squarish"
                  alt="用户头像"
                  class="w-12 h-12 rounded-full object-cover mr-4"
                />
                <div>
                  <h4 class="font-bold text-blue-900">Ahmed Hassan</h4>
                  <p class="text-gray-500 text-sm">科技创业公司创始人</p>
                </div>
              </div>
              <p class="text-gray-600">
                "Brimail
                的智能分类功能大大提高了我们的工作效率，跨境通信再也不是问题，强烈推荐！"
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- "一带一路"专题 -->
    <section class="py-20 bg-white">
      <div class="container mx-auto px-6">
        <div class="flex flex-col md:flex-row items-center">
          <div class="md:w-1/2 mb-10 md:mb-0 md:pr-10">
            <h2 class="text-3xl font-bold text-blue-900 mb-6">
              "一带一路"精神
            </h2>
            <p class="text-gray-600 mb-6">
              Brimail
              秉承"一带一路"倡议的互联互通、共建共享理念，致力于打造连接东西方的数字桥梁，推动全球信息交流与合作。
            </p>
            <p class="text-gray-600 mb-6">
              我们的服务网络覆盖"一带一路"沿线国家和地区，为各国企业和个人用户提供安全、高效、智能的邮件服务，助力全球化发展。
            </p>
            <div class="flex flex-wrap gap-4">
              <button
                class="bg-blue-900 hover:bg-blue-800 text-white font-bold py-3 px-8 !rounded-button whitespace-nowrap cursor-pointer"
              >
                了解 Bri 精神
              </button>
              <button
                class="bg-transparent border-2 border-blue-900 hover:bg-blue-900/5 text-blue-900 font-bold py-3 px-8 !rounded-button whitespace-nowrap cursor-pointer"
              >
                全球合作案例
              </button>
            </div>
          </div>
          <div class="md:w-1/2">
            <img
              src="https://readdy.ai/api/search-image?query=Digital%20Silk%20Road%20concept%20with%20Asia%20on%20the%20left%20and%20Americas%20on%20the%20right%2C%20modern%20visualization%20without%20country%20borders%2C%20showing%20global%20digital%20connections%20across%20Pacific%20Ocean%2C%20with%20flowing%20data%20streams%2C%20network%20nodes%20in%20blue%20and%20gold%20color%20scheme&width=600&height=400&seq=bri-concept&orientation=landscape"
              alt="数字丝绸之路概念图"
              class="w-full h-auto rounded-xl shadow-xl"
            />
          </div>
        </div>
      </div>
    </section>
    <!-- 行动召唤 -->
    <section
      class="py-16 bg-gradient-to-r from-blue-900 to-blue-800 text-white"
    >
      <div class="container mx-auto px-6 text-center">
        <h2 class="text-3xl font-bold mb-6">开启您的全球通信之旅</h2>
        <p class="text-xl opacity-90 mb-10 max-w-2xl mx-auto">
          加入 Brimail，连接世界各地，享受安全、高效、智能的邮件服务体验。
        </p>
        <button
          class="bg-yellow-500 hover:bg-yellow-600 text-blue-900 font-bold py-3 px-10 !rounded-button text-lg whitespace-nowrap cursor-pointer"
        >
          立即注册
        </button>
      </div>
    </section>
    <!-- 页脚 -->
    <footer class="bg-gray-900 text-white py-16">
      <div class="container mx-auto px-6">
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-10">
          <div>
            <div class="text-2xl font-bold mb-6 flex items-center">
              <el-icon class="mr-2 text-3xl"><Message /></el-icon>
              <span>Brimail</span>
            </div>
            <p class="text-gray-400 mb-6">
              连接东西方的专业邮件服务平台，为全球用户提供安全、高效、智能的跨境通信解决方案。
            </p>
            <div class="flex space-x-4">
              <a href="#" class="text-gray-400 hover:text-white cursor-pointer">
                <el-icon class="text-xl"><Position /></el-icon>
              </a>
              <a href="#" class="text-gray-400 hover:text-white cursor-pointer">
                <el-icon class="text-xl"><ChatDotRound /></el-icon>
              </a>
              <a href="#" class="text-gray-400 hover:text-white cursor-pointer">
                <el-icon class="text-xl"><Share /></el-icon>
              </a>
              <a href="#" class="text-gray-400 hover:text-white cursor-pointer">
                <el-icon class="text-xl"><Link /></el-icon>
              </a>
            </div>
          </div>
          <div>
            <h3 class="text-lg font-bold mb-6">产品服务</h3>
            <ul class="space-y-3">
              <li>
                <a
                  href="#"
                  class="text-gray-400 hover:text-white cursor-pointer"
                  >企业邮箱</a
                >
              </li>
              <li>
                <a
                  href="#"
                  class="text-gray-400 hover:text-white cursor-pointer"
                  >跨境通信</a
                >
              </li>
              <li>
                <a
                  href="#"
                  class="text-gray-400 hover:text-white cursor-pointer"
                  >邮件安全</a
                >
              </li>
              <li>
                <a
                  href="#"
                  class="text-gray-400 hover:text-white cursor-pointer"
                  >智能管理</a
                >
              </li>
              <li>
                <a
                  href="#"
                  class="text-gray-400 hover:text-white cursor-pointer"
                  >API 集成</a
                >
              </li>
            </ul>
          </div>
          <div>
            <h3 class="text-lg font-bold mb-6">关于我们</h3>
            <ul class="space-y-3">
              <li>
                <a
                  href="#"
                  class="text-gray-400 hover:text-white cursor-pointer"
                  >公司简介</a
                >
              </li>
              <li>
                <a
                  href="#"
                  class="text-gray-400 hover:text-white cursor-pointer"
                  >发展历程</a
                >
              </li>
              <li>
                <a
                  href="#"
                  class="text-gray-400 hover:text-white cursor-pointer"
                  >团队介绍</a
                >
              </li>
              <li>
                <a
                  href="#"
                  class="text-gray-400 hover:text-white cursor-pointer"
                  >新闻动态</a
                >
              </li>
              <li>
                <a
                  href="#"
                  class="text-gray-400 hover:text-white cursor-pointer"
                  >加入我们</a
                >
              </li>
            </ul>
          </div>
          <div>
            <h3 class="text-lg font-bold mb-6">支持与帮助</h3>
            <ul class="space-y-3">
              <li>
                <a
                  href="#"
                  class="text-gray-400 hover:text-white cursor-pointer"
                  >帮助中心</a
                >
              </li>
              <li>
                <a
                  href="#"
                  class="text-gray-400 hover:text-white cursor-pointer"
                  >常见问题</a
                >
              </li>
              <li>
                <a
                  href="#"
                  class="text-gray-400 hover:text-white cursor-pointer"
                  >联系我们</a
                >
              </li>
              <li>
                <a
                  href="#"
                  class="text-gray-400 hover:text-white cursor-pointer"
                  >服务条款</a
                >
              </li>
              <li>
                <a
                  href="#"
                  class="text-gray-400 hover:text-white cursor-pointer"
                  >隐私政策</a
                >
              </li>
            </ul>
          </div>
        </div>
        <div
          class="border-t border-gray-800 mt-12 pt-8 flex flex-col md:flex-row justify-between items-center"
        >
          <p class="text-gray-500 mb-4 md:mb-0">
            © 2025 Brimail. 保留所有权利。
          </p>
          <div class="flex items-center space-x-4">
            <a
              href="#"
              class="text-gray-500 hover:text-white cursor-pointer flex items-center"
            >
              <el-icon class="mr-1"><CreditCard /></el-icon>
              <span>Visa</span>
            </a>
            <a
              href="#"
              class="text-gray-500 hover:text-white cursor-pointer flex items-center"
            >
              <el-icon class="mr-1"><Money /></el-icon>
              <span>PayPal</span>
            </a>
            <a
              href="#"
              class="text-gray-500 hover:text-white cursor-pointer flex items-center"
            >
              <el-icon class="mr-1"><Wallet /></el-icon>
              <span>Alipay</span>
            </a>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>
<script lang="ts" setup>
import { ref } from "vue";
import {
  Message,
  ArrowDown,
  Menu,
  Connection,
  Lock,
  ChatDotRound,
  Files,
  Apple,
  Aim,
  Cloudy,
  DataAnalysis,
  Dish,
  Monitor,
  Document,
  AlarmClock,
  Position,
  Share,
  Link,
  CreditCard,
  Money,
  Wallet,
} from "@element-plus/icons-vue";
</script>
<style scoped>
.animate-bounce {
  animation: bounce 2s infinite;
}
@keyframes bounce {
  0%,
  100% {
    transform: translateY(0) translateX(-50%);
  }
  50% {
    transform: translateY(-10px) translateX(-50%);
  }
}
</style>
