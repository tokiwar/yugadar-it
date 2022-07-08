<template>
  <div
    class="flex flex-col justify-center items-center w-screen h-screen font-sans uppercase bg-gradient-to-b from-blue-300 select-none"
    :class="{'space-y-8' : $device.isDesktopOrTablet, 'space-y-4' : $device.isMobile}">
    <span class="font-black text-center"
          :class="{'text-8xl' : $device.isDesktopOrTablet, 'text-4xl' : $device.isMobile}">
      Наш сайт<br>в разработке
    </span>
    <span class="flex flex-row justify-center items-center font-bold"
          :class="{'text-2xl' : $device.isDesktopOrTablet, 'text-base' : $device.isMobile}">
     Скоро открытие
    </span>
    <loading-bar/>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
}
</script>
