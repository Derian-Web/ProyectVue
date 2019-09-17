<template>
    <div>
      <cabezera></cabezera>
       <div class="container" id="bajar">
           <h4 class="d-flex justify-content-start ">Category</h4>
		<div class="d-flex justify-content-start">
			<input class="typeahead form-control" type="text" placeholder="Broswer Category...."
				style="border-top:none;border-left: none;border-right:none;">
			<i class="fas fa-search" style="padding:0;"></i>
		</div>
        <div class="contenedorCate row" >
       <div class="col-3" v-for="categori in Categories" :key="categori.id">
          <category :uuid="categori.uuid" :name="categori.name"></category>
       </div>
    </div>
        </div>
       </div>
</template>
<script>
import Category from "@/components/Category.vue"
import Cabezera from "@/components/Cabezera.vue"
export default {
    name: 'bronscategories',
    components:{
        Category,
        Cabezera
    },
    data() {
    return {
      Categories:{
        Categories:[]
      }

    };
  },
  created() {
    this.getCategorie();  
  },
  methods:{
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