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
    <template #heading>Documentation</template>
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <CommunityIcon />
    </template>
    <template #heading>Community</template>
    <img
      class="blueberry"
      src="../assets/blueberry.png"
      width="90"
      height="90"
    />
    <button v-on:click="redirect_to_login">
      img (class="raz" src="../assets/raz.png" width="80" height="65")
    </button>
    <img class="gg" src="../assets/gg.png" width="60" height="60" />
    <img class="drizzle" src="../assets/drizzle.webp" width="90" height="90" />
    <img class="coco" src="../assets/coco.png" width="90" height="90" />
    <img class="blueraz" src="../assets/blueraz.png" width="90" height="90" />
    <img class="pitaya" src="../assets/pitaya.png" width="90" height="90" />
    <img class="acai" src="../assets/acai.png" width="90" height="90" />
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <SupportIcon />
    </template>
    <template #heading>Support Vue</template>

    As an independent project, Vue relies on community backing for its
    sustainability. You can help us by
  </WelcomeItem>
</template>
