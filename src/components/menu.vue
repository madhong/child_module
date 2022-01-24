<template>
  <a-menu
    id="dddddd"
    v-model:openKeys="openKeys"
    v-model:selectedKeys="selectedKeys"
    style="width: 100%; background-color: rgb(165, 161, 161)"
    mode="inline"
    @click="handleClick"
  >
    <my-sub></my-sub>
  </a-menu>
</template>
<script>
import { defineComponent, ref, watch } from "vue";
import mySub from "./subMenu.vue";
export default defineComponent({
  name: "menu",
  components: {
    mySub,
  },

  setup() {
    const selectedKeys = ref([""]);
    const openKeys = ref(["sub1"]);

    const handleClick = (e) => {
      console.log("click", e);
    };

    const titleClick = (e) => {
      console.log("titleClick", e);
    };

    watch(
      () => openKeys,
      (val) => {
        console.log("openKeys", val);
      }
    );
    return {
      selectedKeys,
      openKeys,
      handleClick,
      titleClick,
    };
  },
});
</script>