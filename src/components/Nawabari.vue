<template>
  <div>
    <div class="front">
      <img :src="maroImg">
    </div>
    <div class="back">
      <img :src="backImg">
    </div>
  </div>
</template>

<script lang="ts">
export default {
  name: 'Demarcation',
  data() {
    return {
      maroImg: require('../assets/maro_01.png'),
      backImg: require('../assets/back_01.jpg'),
    };
  },
};
</script>

<style scoped lang="scss">
.front {
  position: relative;
  z-index: 10;
  width: 960px;
  height: 540px;
  img {
    position: absolute;
    top: 216px;
    right: 32%;
  }
}
.back {
  position: absolute;
  top: 0;
  width: 100%;
  height: 100%;
}
</style>
