<template>
  <a-layout>
    <a-layout-sider>
      <mymenu></mymenu>
    </a-layout-sider>
    <a-layout>
      <a-layout-header>Header</a-layout-header>
      <a-layout-content>Content</a-layout-content>
    </a-layout>
  </a-layout>
</template>
<script>
import { defineComponent } from "vue";
import mymenu from "./menu.vue";
export default defineComponent({
  name: "HelloWorld",
  components: {
    mymenu,
  },
});
</script>