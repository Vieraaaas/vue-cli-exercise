<template>
  <LayoutHeader />
  <router-view />
</template>

<script>
import LayoutHeader from "@/components/LayoutHeader.vue";

export default {
  name: "App",
  components: {
    LayoutHeader,
  },
};
</script>
