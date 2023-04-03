<script>
export default {
  // reactive state
  data() {
    return {
      count: 0,
      items: [],
    };
  },

  // functions that mutate state and trigger updates
  methods: {
    increment() {
      this.count++;
    },
    addItem(itemName) {
      this.items.push(itemName);
      myFunction();
    },
    myFunction() {
      //create a div element
      //var div = document.createElement("div");

      //create an image element
      //var img = document.createElement("img");

      //add image src property
      //img.src = "../assets/blueberry.png";

      //append div as a child to body
      //document.body.appendChild(div);

      //append image as a child to div
      //div.appendChild(img);
      alert("This function ran");
      var elem = document.createElement("img");
      elem.setAttribute("src", "../assets/blueberry.png");
      elem.setAttribute("height", "50");
      elem.setAttribute("width", "50");

      document.getElementById("placehere").appendChild(elem);
    },
  },

  // lifecycle hooks
  mounted() {
    console.log(`The initial count is ${this.count}.`);
  },
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
    @click="addItem('Blueberry')"
    class="blueberry"
    src="../assets/blueberry.png"
    width="90"
    height="90"
  />
  <img
    @click="addItem('Strawberry')"
    class="strw"
    src="../assets/strw.png"
    width="110"
    height="70"
  />
  <img
    @click="addItem('Gronola')"
    class="gg"
    src="../assets/gg.png"
    width="60"
    height="60"
  />
  <img
    @click="addItem('Banana')"
    class="ban"
    src="../assets/ban.png"
    width="80"
    height="60"
  />
  <img
    @click="addItem('Chocolate drizzle')"
    class="choc"
    src="../assets/choc.png"
    width="90"
    height="80"
  />
  <img
    @click="addItem('Honey')"
    class="drizzle"
    src="../assets/drizzle.webp"
    width="90"
    height="80"
  />

  <img
    @click="addItem('coconut base')"
    class="coco"
    src="../assets/coco.png"
    width="90"
    height="90"
  />
  <img
    @click="addItem('bluerazz base')"
    class="blueraz"
    src="../assets/blueraz.png"
    width="95"
    height="90"
  />
  <img
    @click="addItem('pitaya base')"
    class="pitaya"
    src="../assets/pitaya.png"
    width="95"
    height="90"
  />
  <img
    @click="addItem('acai base')"
    class="acai"
    src="../assets/acai.png"
    width="90"
    height="90"
  />
  <img
    @click="addItem('greenz base')"
    class="greenz"
    src="../assets/green.png"
    width="90"
    height="90"
  />
  <ul id="list">
    <li v-for="item in items">{{ item }}</li>
  </ul>
  <button class="clear" onclick="clear()">reset order</button>
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
</style>
