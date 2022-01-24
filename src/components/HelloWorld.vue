<template>
  <a-menu
    id="dddddd"
    v-model:openKeys="openKeys"
    v-model:selectedKeys="selectedKeys"
    style="width: 256px"
    mode="inline"
    @click="handleClick"
  >
    <a-sub-menu key="sub1" @titleClick="titleClick">
      <template #icon>
        <MailOutlined />
      </template>
      <template #title>目录 one</template>
      <a-menu-item-group key="g1">
        <template #icon>
          <QqOutlined />
        </template>
        <template #title>Item 1</template>
        <a-menu-item key="1">菜单 1</a-menu-item>
        <a-menu-item key="2">菜单 2</a-menu-item>
      </a-menu-item-group>
      <a-menu-item-group key="g2" title="Item 2">
        <a-menu-item key="3">菜单 3</a-menu-item>
        <a-menu-item key="4">菜单 4</a-menu-item>
      </a-menu-item-group>
    </a-sub-menu>
  </a-menu>
</template>
<script>
import { defineComponent, ref, watch } from "vue";
import { MailOutlined, QqOutlined } from "@ant-design/icons-vue";
export default defineComponent({
  name: "HelloWorld",
  components: {
    MailOutlined,
    QqOutlined,
  },

  setup() {
    const selectedKeys = ref(["1"]);
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