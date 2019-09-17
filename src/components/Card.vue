<template>
   <div class="card" style="height: 100%">
    <div class="overflow-auto contenedor_card" style="height:150px;">
       <router-link class="text-decoration-none" :to="'../Product/'+uuid">
        <img :src="image" class="card-img-top mx-auto d-block" style="width:95% ; " alt="..." />
      </router-link>  
    </div>
    <div class="card-body">
      <h5 class="card-title">{{name}}</h5>
      <br />
      <p class="card-text">{{description}}</p>
    </div>

    <div class="p-4">
      <a :href="url" target="_blank" rel="noopener noreferrer">
        <input
          type="button"
          value="Visit site"
          class="btn btn-block border-dark pure-button pure-button-active bg-white"
        />
      </a>
    </div>
    <br />
    <br />
  </div>
</template>

<script>
export default {
  name: "Card",
  props: ["name",
  "description",
  "image",
  "url",
  "uuid"
  ],
  
  
}
</script>