<template>
  <navbar
    :pages="pages"
    :active-page="activePage"
    :nav-link-click="(index) => (activePage = index)"
  ></navbar>
  <page-view :page="pages[activePage]"></page-view>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import PageView from "./components/PageView.vue";

export default {
  components: {
    Navbar,
    PageView,
  },
  data() {
    return {
      activePage: 0,
      pages: [
        {
          link: { text: "Home", url: "index.html" },
          pageTitle: "Home Page",
          content: "This is the home content",
        },
        {
          link: { text: "About", url: "index.html" },
          pageTitle: "About Page",
          content: "This is the about content",
        },
        {
          link: { text: "Contact", url: "index.html" },
          pageTitle: "Contact Page",
          content: "This is the contact content",
        },
      ],
    };
  },
};
</script>
