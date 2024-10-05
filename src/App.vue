<template>
  <div class="w-full h-[5000px]" style="background: linear-gradient(to bottom, white, lightyellow, orange);">
    <div class="h-screen">
      <div class="flex flex-col px-64 mt-5 w-full">
        <div class="float-left">
          <img src="./assets/dromara.png" class="w-40 flex" />
        </div>
        <div class="flex flex-row w-full">
          <div class="flex flex-col mt-32">
            <transition appear name="slide-fade">
              <div v-show="show" class="text-[150px] text-amber-700 font-bold animate-item" style="--delay: 0s;">CosCon
                2024</div>
            </transition>
            <transition appear name="slide-fade">
              <div v-show="show" class="text-4xl text-amber-700 font-bold pl-5 animate-item" style="--delay: 0.5s;">
                Dromara分会场</div>
            </transition>
          </div>
          <div class="flex justify-center items-center pt-[300px] pl-[300px]">
            <div class="w-[300px] h-[300px]">
              <img src="./assets/qrcode.png" class="w-full h-full object-cover" alt="QR Code" />
            </div>
          </div>
        </div>
        <hr class="border-white mt-20" />
        <div class="flex flex-col">
          <transition appear name="slide-fade">
            <div v-show="show" class="text-5xl text-amber-700 font-bold pl-5 animate-item" style="--delay: 1s;">Beijing
              / 北京</div>
          </transition>
          <transition appear name="slide-fade">
            <div v-show="show" class="text-3xl text-amber-700 font-bold pl-5 animate-item" style="--delay: 1.5s;">
              2024.11.2</div>
          </transition>
        </div>
      </div>
      <div class="flex items-center justify-center">
        <div @click="scrollToView()"
          class="border-4 border-amber-700 w-[180px] h-[75px] rounded-lg items-center justify-center flex text-amber-700 font-bold text-xl mt-12 select-none hover:bg-amber-100">
          开启变革</div>
      </div>
    </div>

    <div class="text-[80px] text-amber-600 font-bold items-center flex justify-center mt-20" id="des">大会介绍</div>
    <div class="text-xl text-amber-600 font-bold items-center flex justify-center mt-20 px-[300px]" id="des">
      中国开源年会（COSCon）是业界最具影响力的开源盛会之一，自2015年由开源社首次发起以来，今年即将迎来第九届。凭借其独特定位及不断增长的影响力，COSCon
      不仅获得了越来越多国内外企业、高校以及开源组织和社区的鼎力支持，而且与一般由企业、IT
      媒体或行业协会举办的行业大会相比，它拥有更广泛的跨组织、跨项目、跨社区的覆盖范围，因此成功吸引了大量来自全球的开源开发者、贡献者和提交者的高度关注与积极参与。
    </div>

    <div class="text-[80px] text-amber-600 font-bold items-center flex justify-center mt-20" id="des">大会地址</div>
    <div class="text-[30px] text-amber-600 font-bold items-center flex justify-center" id="des">北京中关村国家自主创新示范区会议中心
    </div>
    <div class="text-xl text-amber-600 font-bold items-center flex justify-center mt-20 px-[300px]" id="des">
      <iframe
        src="https://m.amap.com/navi/?dest=116.293344,39.989479&destName=北京中关村国家自主创新示范区会议中心&hideRouteIcon=1&key=584d85ce77e3a854180cd921c9a41977&jscode=bb0d66965cd65d1f4678312df26b9e37"
        class="w-full h-[1000px]" />
    </div>

    <div class="text-[80px] text-amber-600 font-bold items-center flex justify-center mt-20" id="des">演讲成员</div>
    <div class="text-2xl text-amber-600 font-bold items-center flex justify-center mt-20 px-[300px]" id="des">
      <div class="w-full">
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

    <div class="text-[80px] text-amber-600 font-bold items-center flex justify-center mt-20" id="des">时间线</div>
    <div class="text-[30px] text-amber-600 font-bold items-center flex justify-center" id="des">待定</div>

    <!-- <div class="text-[80px] text-amber-600 font-bold items-center flex justify-center mt-20" id="des">组织成员项目</div>
    <div class="mt-20 flex flex-row p-10">
      <img :src="url" v-for="url in [
        './assets/Akali.webp',
        './assets/logos/CloudEon.webp',
        './assets/logos/cubic.webp',
        './assets/logos/dante-cloud.webp',
        './assets/logos/dax-pay.webp',
        './assets/logos/dbswitch.webp'
      ]" class="w-[200px] p-3"/>
    </div> -->
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
