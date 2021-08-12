<template>
  <div class="header">
    <div class="name">
      <h1>{{ title }}</h1>
      <p>The home for you</p>
    </div>
    <div id="links">
      <ul v-bind:key="link" v-for="link in links">
        <a :href="`../pages/${link.link}`"> {{ link.name }}</a>
      </ul>
      <div>
        <span id="devider">|</span>
        <a href="#"><i class="fa fa-search"></i></a>
        <a href="#"><i class="fa fa-shopping-cart"></i></a>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Header",
  props: {
    title: String,
  },
  data() {
    return {
      links: [
        { name: "Home", link: "Home.vue" },
        { name: "About", link: "Abour.vue" },
      ],
    };
  },
};
</script>
<style scoped>
.header {
  display: flex;
  justify-content: space-between;
  background-color: #ffefd3;
  padding: 2rem;
  color: #c03553;
  align-items: center;
}
#links {
  display: flex;
}
h1 {
  font-size: 3rem;
}
a {
  text-decoration: none;
  font-size: 20px;
  color: #c03553;
  padding: 2px;
}
a:hover {
  border-bottom: 3px solid;
}
#devider {
  padding-inline: 15px;
}
</style>