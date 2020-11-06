<template>
  <div class="zoshoku">
    <div>
      <img src="../assets/maro.jpg">
    </div>
    <router-link to="/">
      <button>もどる</button>
    </router-link>
  </div>
</template>

<script>
export default {
name: 'Zoshoku',
};
</script>

<style scoped lang="scss">
.zoshoku {
  text-align: center;
}
</style>
