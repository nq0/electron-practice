<template>
<div class="frame">
  <div class="top">

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
name: "HomeFrame",
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
      ]
    }
  },
  methods: {
    clickButton(item: number) {
      console.log(item)
    }
  }
}
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
}

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
</style>
