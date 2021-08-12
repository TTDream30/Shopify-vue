<template>
  <div class="container" :key="product" v-for="product in products">
    <div class="card">
      <div>
        <img :src="require(`../assets/${product.link}`)" />
      </div>
      <div class="card-info">
        <p>Name: {{ product.name }}</p>
        <br />
        Price:
        <span style="color: red">${{ product.price }}</span>
        <br /><br />
        <Button text="Add to Cart" />
      </div>
    </div>
  </div>
</template>
<script>
import Button from "./Button.vue";
export default {
  name: "Content",
  components: {
    Button,
  },
  props: {},
  data() {
    return {
      products: [
        { name: "Hoodie", price: 46.0, link: "hoodie.jpg" },
        { name: "Pants", price: 43.0, link: "pants.jpg" },
      ],
    };
  },
};
</script>
<style scoped>
.container {
  display: inline-flex;
  flex-wrap: wrap;
}
.card {
  margin: 2rem;
  display: block;
  overflow: hidden;
  border-radius: 12px;
  box-shadow: 2px 2px 2px gray;
  width: 15rem;
  height: 24rem;
}
.card:hover {
  cursor: pointer;
  box-shadow: 4px 4px 4px gray;
}
.card img {
  width: 20rem;
  height: 15rem;
  object-fit: cover;
}
.card-info {
  padding: 12px;
  text-align: center;
  justify-content: space-between;
}
</style>