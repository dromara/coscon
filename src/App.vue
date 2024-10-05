<template>
  <div class="w-full min-h-screen" style="background: linear-gradient(to bottom, white, lightyellow, orange);">
    <div class="flex flex-col px-4 sm:px-8 md:px-16 lg:px-32 xl:px-64 w-full h-screen">
      <div class="float-left mt-4">
        <img src="./assets/dromara.png" class="w-20 sm:w-32 md:w-40 flex" />
      </div>
      <div class="flex flex-col lg:flex-row w-full mt-8 lg:mt-16">
        <div class="flex flex-col">
          <transition appear name="slide-fade">
            <div v-show="show" class="text-4xl sm:text-6xl md:text-7xl lg:text-[80px] text-amber-700 font-bold animate-item" style="--delay: 0s;">CosCon 2024</div>
          </transition>
          <transition appear name="slide-fade">
            <div v-show="show" class="text-xl sm:text-2xl md:text-3xl lg:text-4xl text-amber-700 font-bold animate-item" style="--delay: 0.5s;">Dromara分会场</div>
          </transition>
        </div>
        <div class="flex justify-center items-center mt-8 lg:mt-0 lg:ml-auto">
          <div class="w-40 h-40 sm:w-60 sm:h-60 md:w-80 md:h-80 lg:w-[300px] lg:h-[300px]">
            <img src="./assets/qrcode.png" class="w-full h-full object-cover" alt="QR Code" />
          </div>
        </div>
      </div>
      <hr class="border-white mt-8 lg:mt-20" />
      <div class="flex flex-col mt-4 lg:mt-8">
        <transition appear name="slide-fade">
          <div v-show="show" class="text-2xl sm:text-3xl md:text-4xl lg:text-5xl text-amber-700 font-bold animate-item" style="--delay: 1s;">Beijing / 北京</div>
        </transition>
        <transition appear name="slide-fade">
          <div v-show="show" class="text-xl sm:text-2xl md:text-2xl lg:text-3xl text-amber-700 font-bold mt-2 animate-item" style="--delay: 1.5s;">2024.10.2</div>
        </transition>
      </div>
      <div class="flex items-center justify-center">
        <div @click="scrollToView()"
          class="border-4 border-amber-700 w-[180px] h-[75px] rounded-lg items-center justify-center flex text-amber-700 font-bold text-xl mt-12 select-none hover:bg-amber-100">
          开启变革</div>
      </div>
    </div>
    
    <!-- 其他部分的移动端适配 -->
    <div class="px-4 sm:px-8 md:px-16 lg:px-32 xl:px-64">
      <div class="text-4xl sm:text-5xl md:text-6xl lg:text-[80px] text-amber-600 font-bold items-center flex justify-center mt-20" id="des">大会介绍</div>
      <div class="text-base sm:text-lg md:text-xl text-amber-600 font-bold items-center flex justify-center mt-10 sm:mt-20">
        中国开源年会（COSCon）是业界最具影响力的开源盛会之一，自2015年由开源社首次发起以来，今年即将迎来第九届。凭借其独特定位及不断增长的影响力，COSCon
        不仅获得了越来越多国内外企业、高校以及开源组织和社区的鼎力支持，而且与一般由企业、IT
        媒体或行业协会举办的行业大会相比，它拥有更广泛的跨组织、跨项目、跨社区的覆盖范围，因此成功吸引了大量来自全球的开源开发者、贡献者和提交者的高度关注与积极参与。
      </div>

      <div class="text-4xl sm:text-5xl md:text-6xl lg:text-[80px] text-amber-600 font-bold items-center flex justify-center mt-20" id="des">大会地址</div>
      <div class="text-xl sm:text-2xl md:text-[30px] text-amber-600 font-bold items-center flex justify-center text-center mt-5">北京中关村国家自主创新示范区会议中心</div>
      <div class="mt-10 sm:mt-20">
        <iframe
          src="https://m.amap.com/navi/?dest=116.293344,39.989479&destName=北京中关村国家自主创新示范区会议中心&hideRouteIcon=1&key=584d85ce77e3a854180cd921c9a41977&jscode=bb0d66965cd65d1f4678312df26b9e37"
          class="w-full h-[300px] sm:h-[500px] md:h-[700px] lg:h-[1000px]" />
      </div>

      <div class="text-4xl sm:text-5xl md:text-6xl lg:text-[80px] text-amber-600 font-bold items-center flex justify-center mt-20" id="des">演讲成员</div>
      <div class="text-base sm:text-lg md:text-xl lg:text-2xl text-amber-600 font-bold items-center flex justify-center mt-10 sm:mt-20">
        <div class="w-full overflow-x-auto">
          <table class="w-full border-amber-600 border-2">
            <tr class="w-full border-amber-600 border-2">
              <td>猫大人（负责人）</td>
              <td>唯一解（演讲嘉宾）</td>
              <td>阿超（演讲嘉宾）</td>
              <td>风如歌（演讲嘉宾）</td>
              <td>Acbox（演讲嘉宾）</td>
            </tr>
            <tr class="w-full border-amber-600 border-2">
              <td>NicholasLD</td>
              <td>萧帽</td>
              <td>付守江</td>
              <td>疯狂的狮子Li</td>
              <td>读钓</td>
              <td>mouday</td>
            </tr>
            <tr class="border-amber-600 border-2">
              <td>失败女神</td>
              <td>唐振超（方糖先生）</td>
              <td>yanhom</td><td>sh1yu</td>
              <td>小眼</td>
            </tr>
          </table>
        </div>
      </div>

      <div class="text-4xl sm:text-5xl md:text-6xl lg:text-[80px] text-amber-600 font-bold items-center flex justify-center mt-20" id="des">时间线</div>
      <div class="text-xl sm:text-2xl md:text-[30px] text-amber-600 font-bold items-center flex justify-center">待定</div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      show: false,
      scrollToView() {
        const element = document.getElementById('des');
        if (element)
          element.scrollIntoView({ behavior: 'smooth' });
      }
    }
  },
  mounted() {
    this.show = true;
  }
}
</script>

<style scoped>
.animate-item {
  animation: slideUp 1s ease-out var(--delay) both;
}

@keyframes slideUp {
  from {
    transform: translateY(20px);
    opacity: 0;
  }

  to {
    transform: translateY(0);
    opacity: 1;
  }
}

.slide-fade-enter-active {
  transition: all 0.8s ease;
}

.slide-fade-enter-from {
  transform: translateY(20px);
  opacity: 0;
}
</style>