<script setup>
import WelcomeItem from "./WelcomeItem.vue";
import DocumentationIcon from "./icons/IconDocumentation.vue";
import CommunityIcon from "./icons/IconCommunity.vue";
import SupportIcon from "./icons/IconSupport.vue";
</script>

<template>
  <WelcomeItem>
    <template #icon>
      <DocumentationIcon />
    </template>

    <h1 class="heading">MAKE UR OWN ACAI BOWL! :))</h1>
    <img
      class="blueberry"
      src="../assets/blueberry.png"
      width="90"
      height="90"
    />
    <img class="strw" src="../assets/strw.png" width="110" height="70" />
    <img class="gg" src="../assets/gg.png" width="60" height="60" />
    <img class="choc" src="../assets/choc.png" width="90" height="90" />
    <img class="drizzle" src="../assets/drizzle.webp" width="90" height="90" />
    <img class="coco" src="../assets/coco.png" width="90" height="90" />
    <img class="blueraz" src="../assets/blueraz.png" width="90" height="90" />
    <img class="pitaya" src="../assets/pitaya.png" width="90" height="90" />
    <img class="greenz" src="../assets/green.png" width="90" height="90" />
    <img class="acai" src="../assets/acai.png" width="90" height="90" />
  </WelcomeItem>
  <p class="p">
    choose ur toppings and watch ur acai bowl being made right on front of u!
  </p>
</template>
<style scoped>
.heading {
  color: deeppink;
  font-family: Trattatello, fantasy;
  font-weight: bold;
}
.p {
  color: black;
  font-family: monospace;
  font-weight: bold;
  margin-left: 80px;
  display: flex;
  text-align: center;
  font-size: large;
}
</style>
