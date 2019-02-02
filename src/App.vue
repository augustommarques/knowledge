<template>
  <div id="app" :class="{ 'hide-menu': !isMenuVisible || !user }">
    <Header
      title="First project Vue"
      :hideToggle="!user"
      :hideUserDropdown="!user"
    ></Header>
    <Menu v-if="user" />
    <Loading v-if="validatingToken" />
    <Content v-else></Content>
    <Footer />
  </div>
</template>

<script>
import Header from "./components/template/Header";
import Menu from "./components/template/Menu";
import Loading from "./components/template/Loading";
import Content from "./components/template/Content";
import Footer from "./components/template/Footer";
// import axios from "axios";

export default {
  name: "App",
  components: {
    Header,
    Menu,
    Loading,
    Content,
    Footer,
  },
};
</script>

<style></style>
