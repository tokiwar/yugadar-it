<template>
  <div class="flex flex-col space-y-4">
    <div class="bg-white" :class="{'h-12 w-96' : $device.isDesktopOrTablet, 'h-8 w-72' : $device.isMobile}">
      <div class="bg-black h-full w-0" :style="{'width' : `${start}%`}"/>
    </div>
    <div class="w-full flex flex-row justify-between items-center">
      <span>0%</span>
      <span>100%</span>
    </div>
  </div>
</template>
<script>
export default {
  name: 'LoadingBar',
  data: () => ({
    start: 0,
    end: 87,
    total: 100
  }),
  methods: {
    progress() {
      this.start += 1;
      if (this.start < this.end) {
        setTimeout(this.progress, 50);
      }
    }
  },
  mounted() {
    this.progress();
  }
}
</script>
