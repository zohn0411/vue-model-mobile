<template>
  <div class="home-container">
    <main class="home-main">
      <router-view />
    </main>
    <footer>
      <Tabbar :tabList="tabList"></Tabbar>
    </footer>
  </div>
</template>

<script>
// @ is an alias to /src
import Tabbar from "@/components/tabbar/tabbar.vue";

export default {
  name: "home",
  components: {
    Tabbar
  },
  data() {
    return {
      tabList: [
        {
          title: "page01",
          path: "/",
          icon: "",
          icon_press: ""
        },
        {
          title: "page02",
          path: "/page02",
          icon: "",
          icon_press: ""
        },
        {
          title: "page03",
          path: "/page03",
          icon: "",
          icon_press: ""
        },
        {
          title: "page04",
          path: "/page04",
          icon: "",
          icon_press: ""
        }
      ]
    };
  }
};
</script>

<style lang="less" scoped>
.home-container {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
}
.home-main {
  flex: 1;
  overflow-y: scroll;
  -webkit-overflow-scrolling: touch;
  scroll-behavior: smooth;
}
footer {
  // width: 100%;
  // position: fixed;
  // bottom: 0;
  // right: 0;
  // left: 0;
  height: 50px;
  line-height: 50px;
  font-size: 16px;
}
</style>
