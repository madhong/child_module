<template>
  <a-menu
    id="dddddd"
    v-model:openKeys="openKeys"
    v-model:selectedKeys="selectedKeys"
    style="width: 100%; background-color: rgb(165, 161, 161)"
    mode="inline"
    @click="handleClick"
  >
    <a-sub-menu key="sub1" @titleClick="titleClick">
      <template #icon>
        <MailOutlined />
      </template>
      <template #title>子项目 one</template>
      <a-menu-item key="1">菜单 1</a-menu-item>
      <a-menu-item key="2">菜单 2</a-menu-item>
    </a-sub-menu>
  </a-menu>
</template>
<script>
import { defineComponent, ref, watch } from "vue";
import { MailOutlined } from "@ant-design/icons-vue";
export default defineComponent({
  name: "menu",
  components: {
    MailOutlined,
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