<template>
<div class="frame">
  <div class="top">
    <ul>
      <li>
        下僕レベル 100Lv
      </li>
      <li>
        かりかり
        <img src="../assets/pet_food_cat.png">
      </li>
      <li>
        ちゅ〜る
        <img src="../assets/thuru.png">
      </li>
      <li>
        かんづめ
        <img src="../assets/pet_food_cat_can.png">
      </li>
      <li>
        にぼし
        <img src="../assets/food_niboshi.png">
      </li>
    </ul>
  </div>
  <div class="left">
    <p>ねこ</p>
  </div>
  <div class="right">
    <ul>
      <li v-for="(item, index) in items">
        <button @click="clickButton(index)">
          <p>{{ item }}</p>
        </button>
      </li>

    </ul>
  </div>
</div>
</template>

<script lang="ts">
export default {
name: 'HomeFrame',
  data() {
    return {
      items: [
        'いち',
        'にー',
        'さん',
        'よん',
        'ごー',
        'ろく',
        'なな',
      ],
    };
  },
  methods: {
    clickButton(i: number) {
      switch (i) {
        case 0: this.$router.push('/zoshoku');
        default: console.log(i);
      }
    },
  },
};
</script>

<style scoped lang="scss">
.frame {
  width: 960px;
  height: 540px;
  z-index: 100;
  position: fixed;
}
.top {
  width: 100%;
  height: 6%;
  background: darkseagreen;
  box-shadow: 0 6px 3px -3px #0000002e;
ul {
    height: 32px;
    align-items: center;
    margin: 0;
    display: flex;
    justify-content: space-around;
    padding: 0 14% 0 10%;
    list-style-type: none;
    li {
      display: flex;
      align-items: center;
      img {
        height: 32px;
      }
    }
  }
}
.left {
  width: 10%;
  height: 100%;
  background: bisque;
  top: 0;
  position: absolute;
  p {
    writing-mode: vertical-rl;
    margin: 30px auto 0;
  }
}
.right {
  position: absolute;
  top: 0;
  right: 0;
  width: 14%;
  height: 100%;
  background: cadetblue;
  ul {
    list-style-type: none;
    margin: 0;
    padding: 16px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    height: 94%;
  }
  button {
    width: 100%;
  }
}
</style>
