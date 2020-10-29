<template>
  <div class="home">
    <HomeFrame/>
    <Nawabari/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import HomeFrame from '@/components/HomeFrame.vue';
import Nawabari from '@/components/Nawabari.vue'; // @ is an alias to /src

@Component({
  components: {
    Nawabari,
    HomeFrame,
  },
})
export default class Home extends Vue {}
</script>

<style lang="scss">
.home {
  width: 960px;
  height: 540px;
}
</style>
