<template>
    <div>
      <cabezera></cabezera>
        <div class="container" id="bajar">
        <div class="row m-0">
            <div class="col-12 col-md-6">
                <h1 id="title">{{Products.name}}</h1>
                <h3 class="color" id="descripcion">{{Products.description}}</h3>
            </div>
            <div class=" col-12 col-md-6 " id="iframe">
                <div id="libro">
                     <img :src="Products.image"
                        alt=""> 
                </div>
            </div>
            <div class="col-md-6" id="bt">
                <button type="button" class="btn btn-dark" id="boton">Visit Website</button>
                <a href="" id="compartir">Share</a>
                <a href="" class="iconn" ><i class="fab fa-twitter"></i></a>
                <a href="" class="iconn"><i class="fab fa-facebook-f"></i></a>
            </div>
        </div>
    </div>
    </div>
</template>
<script>
import Cabezera from "@/components/Cabezera.vue"
export default {
    name: 'Product',
    components:{
      Cabezera
    },
     data() {
    return {
      Products:{
        Products:[]
      }

    };
  },
  created() {
    this.getProducts();  
  },
  methods:{
     getProducts() {
    const url = `http://fundamentos.academlo.com/api/v1/products/${this.$route.params.id}`;
    console.log(url)
    axios
      .get(url)
      .then(response => {
        this.Products = response.data;
        console.log(this.Products);
      })
      .catch(error => {
        console.log(error.response);
        alert("Tuvimos un error cargando la información");
      });
    },
  }
}
</script>
<style  scoped>
@media screen and (max-width: 800px) {
  #descripcion {
    font-size: 12px;
  }
}

@media screen and (max-width: 576px) {
  #pou {
    position: relative;
    top: 400px;
  }
  #bajar {
    margin-left: -35px;
  }
  #bt {
    padding: 120px 0px;
  }
  #bt #boton {
    padding: 5px 30px;
    font-size: 16px;
    position: relative;
    left: 50px;
  }
  #bt a {
    display: none;
  }
  #posicion {
    position: relative;
    top: 350px;
  }
}

@media screen and (max-width: 450px) {
  #pou {
    position: relative;
    top: 400px;
  }
}

@media screen and (max-width: 400px) {
  #pou {
    position: relative;
    top: 500px;
  }
}

@media screen and (max-width: 340px) {
  #pou {
    position: relative;
    top: 520px;
  }
}

* {
  margin: 0;
  padding: 0;
}

#bajar {
  padding-top: 6rem;
  padding-left: 80px;
  height: 550px;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
}

.color {
  color: #585858;
  font-weight: 400;
  font-size: 1rem;
}

#bt {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-pack: center;
      -ms-flex-pack: center;
          justify-content: center;
  -webkit-box-align: center;
      -ms-flex-align: center;
          align-items: center;
  height: auto;
  margin-top: -80px;
}

#bt button {
  background: #fff;
  color: #000;
  font-weight: 600;
  height: 50px;
  margin-right: 50px;
}

#bt a {
  float: right;
  margin: 0px 10px;
}

#bt #compartir {
  color: #585858;
  text-decoration: none;
}

.iconn {
  text-decoration: none;
  color: #585858;
  border: 1px solid #000000;
  border-radius: 50%;
  padding: 8px 12px;
  width: 40px;
  height: 40px;
}

.iconos a {
  color: #7d8985;
  border: 1px solid #7d8985;
  font-size: 20px;
  padding: 10px 15px;
  border-radius: 50%;
  float: right;
  position: relative;
  top: 165px;
}

.espacio {
  position: relative;
  left: 10px;
}

.compartir {
  position: relative;
  left: 350px;
  top: 220px;
  font-weight: 600;
  font-size: 16px;
}

.derecha {
  float: right;
}

.border-1 {
  border: 1px solid #f2f2f2;
}

footer {
  background: #F2F2F2;
  height: 105px;
}

.arriba {
  position: relative;
  top: -25px;
}

#libro {
  overflow: auto;
  width: 100%;
  height: 420px;
}

#libro img {
  width: 100%;
  border: solid 1px #f2f2f2;
}

#libro::-webkit-scrollbar {
  width: 12px;
}

#libro::-webkit-scrollbar-thumb {
  background: #D8D8D8;
  border-radius: 5px;
}

#espacio {
  position: relative;
  top: 15px;
  right: 150px;
}
</style>