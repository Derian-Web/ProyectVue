<template>
  <div>
    <cabezera></cabezera>
    <div class="container mt-5 pt-5 mb-5">
      <h3 class="ml-3 pb-3 font-weight-bold">Productos de {{ProductsCategori.name}}</h3>
      <div class="row m-0">
        <div class="col-sm-12 col-lg-4 mb-5" v-for="product in Products" :key="product.id">
          <card
            :name="product.name"
            :description="product.description"
            :image="product.image"
            :uuid="product.uuid"
            :url="product.url"
          ></card>
          <!-- <card :category="category" ></card> -->
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import Card from "../components/Card.vue";
import Cabezera from "@/components/Cabezera.vue";
export default {
  name: "CategoriProduct",
  components: {
    Cabezera,
    Card
  },
  data() {
    return {
      Products: {
        Products: []
      },
      ProductsCategori: []
    };
  },
  created() {
    this.getProducts();
  },
  methods: {
    getProducts() {
      const url = `http://fundamentos.academlo.com/api/v1/categories/${this.$route.params.id}/products`;
      console.log(url);
      axios
        .get(url)
        .then(response => {
          this.Products = response.data.products;
          this.ProductsCategori = response.data;
          console.log(this.Products);
        })
        .catch(error => {
          console.log(error.response);
          alert("Tuvimos un error cargando la información");
        });
    }
  }
};
</script>
