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
</script>

<template>
  <div
    id="newItems"
    style="
      z-index: 1;
      position: absolute;
      left: 50px;
      top: 50px;

      width: 150%;
      height: 150px;
      padding: 0px;
      color: white;
    "
  ></div>
  <div class="allItems">
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
      @click="addItem('../src/assets/choc.png')"
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
      @click="addItem('../src/assets/blueraz.png')"
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
    <button @click="addItem('../src/assets/bowl.png')" class="clear">
      restart order!
    </button>
  </div>
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
      width="250"
      height="250"
      class="item"
    />
  </header>
</template>
<style scoped>
.clear {
  background-color: black;
  color: white;
  font-family: fantasy;
  font-size: 20px;
  margin-bottom: 10px;
}
.bowl {
  position: relative;
  margin-left: 110px;
  z-index: 1;
  margin-bottom: 10px;
}
.h {
  position: absolute;
  margin-left: 170px;
  margin-top: 90px;
  z-index: 2;
  font-family: fantasy;
  font-weight: bold;
  color: white;
  text-align: center;
  width: 200px;
}

.allItems {
  margin-left: 25%;
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
  top: 40px;
  left: 150px;
  z-index: 3;
}
</style>
