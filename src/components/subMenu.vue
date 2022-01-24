<template>
  <a-sub-menu key="sub1" @titleClick="titleClick">
    <template #icon>
      <MailOutlined />
    </template>
    <template #title>子项目 one</template>
    <a-menu-item key="1">菜单 1</a-menu-item>
    <a-menu-item key="2">菜单 2</a-menu-item>
  </a-sub-menu>
</template>
<script>
import { defineComponent } from "vue";
import { MailOutlined } from "@ant-design/icons-vue";
export default defineComponent({
  name: "mySub",
  components: {
    MailOutlined,
  },

  setup() {
    const titleClick = (e) => {
      console.log("titleClick", e);
    };

    return {
      titleClick,
    };
  },
});
</script>