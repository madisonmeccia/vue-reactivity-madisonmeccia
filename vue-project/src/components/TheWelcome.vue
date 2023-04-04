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

      width: 70%;
      height: 150px;
      padding: 0px;
      color: white;
    "
  ></div>
  <div class="allItems">
    <img
      @click="addItem('/images/blueberry.png')"
      class="blueberry"
      src="/images/blueberry.png"
      width="110"
      height="90"
    />
    <img
      @click="addItem('/images/strw.png')"
      class="strw"
      src="/images/strw.png"
      width="110"
      height="70"
    />
    <img
      @click="addItem('/images/gg.png')"
      class="gg"
      src="/images/gg.png"
      width="60"
      height="60"
    />
    <img
      @click="addItem('/images/ban.png')"
      class="ban"
      src="/images/ban.png"
      width="80"
      height="60"
    />
    <img
      @click="addItem('/images/choc.png')"
      class="choc"
      src="/images/choc.png"
      width="90"
      height="80"
    />
    <img
      @click="addItem('/images/drizzle.webp')"
      class="drizzle"
      src="/images/drizzle.webp"
      width="90"
      height="80"
    />

    <img
      @click="addItem('/images/coco.png')"
      class="coco"
      src="/images/coco.png"
      width="90"
      height="90"
    />
    <img
      @click="addItem('/images/blueraz.png')"
      class="blueraz"
      src="/images/blueraz.png"
      width="95"
      height="90"
    />
    <img
      @click="addItem('/images/pitaya.png')"
      class="pitaya"
      src="/images/pitaya.png"
      width="95"
      height="90"
    />
    <img
      @click="addItem('/images/acai.png')"
      class="acai"
      src="/images/acai.png"
      width="90"
      height="90"
    />
    <img
      @click="addItem('/images/green.png')"
      class="greenz"
      src="/images/green.png"
      width="90"
      height="90"
    />
    <button @click="addItem('/bowl1.png')" class="clear">restart order!</button>
  </div>
  <header>
    <h1 class="h">build your dream acai bowl order!</h1>

    <img
      alt="bowl"
      class="bowl"
      src="/images/bowl.png"
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
  width: 200px;
}

.item {
  position: absolute;
  top: 40px;
  left: 150px;
  z-index: 3;
}
</style>
