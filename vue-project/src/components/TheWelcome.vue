<script>
export default {
  // reactive state
  data() {
    return {
      items: [],
    };
  },

  // functions that mutate state and trigger updates
  methods: {
    addItem(itemName) {
      this.items.push(itemName);
    },
  },

  // lifecycle hooks
  mounted() {},
};
function clear() {
  list = "";
}
</script>

<template>
  <div
    id="newItems"
    style="
      z-index: 1;
      position: absolute;
      left: 50px;
      top: 50px;

      width: 100%;
      height: 100px;
      padding: 0px;
      color: white;
    "
  ></div>
  <img
    @click="addItem('../src/assets/blueberry.png')"
    class="blueberry"
    src="../assets/blueberry.png"
    width="110"
    height="90"
  />
  <img
    @click="addItem('../src/assets/strw.png')"
    class="strw"
    src="../assets/strw.png"
    width="110"
    height="70"
  />
  <img
    @click="addItem('../src/assets/gg.png')"
    class="gg"
    src="../assets/gg.png"
    width="60"
    height="60"
  />
  <img
    @click="addItem('../src/assets/ban.png')"
    class="ban"
    src="../assets/ban.png"
    width="80"
    height="60"
  />
  <img
    @click="addItem('../src/assets/ban.png')"
    class="choc"
    src="../assets/choc.png"
    width="90"
    height="80"
  />
  <img
    @click="addItem('../src/assets/drizzle.webp')"
    class="drizzle"
    src="../assets/drizzle.webp"
    width="90"
    height="80"
  />

  <img
    @click="addItem('../src/assets/coco.png')"
    class="coco"
    src="../assets/coco.png"
    width="90"
    height="90"
  />
  <img
    @click="addItem('../src/assets/coco.png')"
    class="blueraz"
    src="../assets/blueraz.png"
    width="95"
    height="90"
  />
  <img
    @click="addItem('../src/assets/pitaya.png')"
    class="pitaya"
    src="../assets/pitaya.png"
    width="95"
    height="90"
  />
  <img
    @click="addItem('../src/assets/acai.png')"
    class="acai"
    src="../assets/acai.png"
    width="90"
    height="90"
  />
  <img
    @click="addItem('../src/assets/green.png')"
    class="greenz"
    src="../assets/green.png"
    width="90"
    height="90"
  />
  <header>
    <h1 class="h">build your dream acai bowl order!</h1>

    <img
      alt="bowl"
      class="bowl"
      src="../assets/bowl.png"
      width="325"
      height="325"
    />

    <img
      v-for="item in items"
      :src="item"
      width="90"
      height="90"
      class="item"
    />
  </header>
  <ul id="list">
    <li v-for="item in items">{{ item }}</li>
  </ul>
</template>
<style scoped>
#list {
  position: absolute;
  font-family: cursive;
  color: maroon;
  text-align: center;
  font-size: large;
}
.clear {
  background-color: mediumslateblue;
  color: white;
  font-family: fantasy;
  font-size: 15px;
}
.bowl {
  position: relative;
  margin-left: 110px;
  z-index: 1;
  margin-bottom: 10px;
}
.h {
  position: absolute;
  margin-left: 150px;
  margin-top: 110px;
  z-index: 2;
  font-family: fantasy;
  font-weight: bold;
  color: white;
  text-align: center;
  width: 250px;
}
.bowlanditems {
  position: relative;
  display: inline;
  border: 4px dotted blue;
  height: 500px;
  width: 500px;
}

.item {
  position: absolute;
  top: 100px;
  left: 225px;
  z-index: 3;
}
</style>
