<template>
  <div class="home">
    <portada></portada>
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    
    <div class="container mt-5 pt-5 mb-5">
        <h3 class="ml-3 pb-3 font-weight-bold">Productos</h3>
        <div class="row m-0 ">
    <div class="col-sm-12 col-lg-4 mb-5" v-for="(product, index) in Products" :key="product.id"  >
        <card  v-if="index < 3"   :name="product.name" :description="product.description" :image="product.image" :url="product.url"  ></card>
        <!-- <card :category="category" ></card> -->
       </div>
        </div>
      </div>


      <div class="container" >
      <h4 class="d-flex justify-content-start ">Category</h4>
		<div class="d-flex justify-content-start">
			<input class="typeahead form-control" type="text" placeholder="Broswer Category...."
				style="border-top:none;border-left: none;border-right:none;">
			<i class="fas fa-search" style="padding:0;"></i>
		</div>
     <div class="contenedorCate row" >
       <div class="col-3" v-for="(categori, index) in Categories" :key="categori.id">
          <category v-if="index < 8" :name="categori.name" :uuid="categori.uuid"></category>
       </div>
    </div>
    </div>
  </div>
</template> 
<script>
// @ is an alias to /src

import Card from "../components/Card.vue"
import Portada from "@/components/Portada.vue"
 import Category from "@/components/Category.vue"
 

export default {
  name: 'home',
  components: {
    Card,
    Portada,
    Category,
  },
  data() {
    return {
      Products: {
        Products: []
      },
      Categories:{
        Categories:[]
      }

    };
  },
  created() {
    this.getProducts();
    this.getCategorie();
  },
  methods: {
   getProducts() {
    const url = "http://fundamentos.academlo.com/api/v1/categories/15b062da-64d2-4565-94ec-1536d4378605/products";
    console.log(url)
    axios
      .get(url)
      .then(response => {
        this.Products = response.data.products;
        console.log(this.Products);
      })
      .catch(error => {
        console.log(error.response);
        alert("Tuvimos un error cargando la información");
      });
    },
    getCategorie() {
       const url = "http://fundamentos.academlo.com/api/v1/directories/4c3190e3-a57f-491e-982e-d6d534db5ff3/categories";
       console.log(url)
       axios
      .get(url)
      .then(response => {
        this.Categories = response.data.categories;
        console.log(this.Categories);
      })
      .catch(error => {
        console.log(error.response);
        alert("Tuvimos un error cargando la información");
      });
      } 
    
  }
}
</script>
