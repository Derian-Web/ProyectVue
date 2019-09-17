<template >
  <div>
    <header>
      <nav class="menu" id="menu2">
        <a href="index.html">
          <img id="logo" src="@/assets/logo.png" alt="Logo" />
        </a>
        <router-link  to="/bronscategories">Explore</router-link>
        <a href="#">ADD A LISTING</a>
      </nav>
      <div class="container2" id="anchura">
        <div class="textos" id="centrado">
          <h1 id="size">ECO-AWARENESS</h1>
          <h2>No tires basura mejor tira barrio</h2>
          <a href="browse-categories.html">Browse Categories</a>
        </div>
        <img class="portada" id="alto-img" src="@/assets/img-1.png" alt />
      </div>
    </header>
    <div class="wave">
      <div style="height: 150px; overflow: hidden;">
        <svg viewBox="0 0 500 150" preserveAspectRatio="none" style="height: 100%; width: 100%;">
          <path
            d="M0.00,49.98 C150.00,150.00 349.20,-50.00 500.00,49.98 L500.00,150.00 L0.00,150.00 Z"
            style="stroke: none; fill: #fff;"
          />
        </svg>
      </div>
    </div>
  </div>
</template>
<style  scoped>
@media screen and (max-width: 800px) {
  .container2 #alto-img {
    height: 300px;
  }
  .container2 #size {
    font-size: 40px;
  }
}

@media screen and (max-width: 576px) {
  #anchura {
    width: 100%;
  }
  .container2 {
    -ms-flex-wrap: wrap-reverse;
    flex-wrap: wrap-reverse;
    -webkit-box-pack: center;
    -ms-flex-pack: center;
    justify-content: center;
  }
  .container2 #alto-img {
    height: 300px;
  }
  #size {
    font-size: 30px;
    text-align: center;
  }
  #menu2 {
    float: right;
  }
  #centrado {
    width: 100%;
    text-align: center;
  }
}

* {
  margin: 0;
  padding: 0;
  -webkit-box-sizing: border-box;
  box-sizing: border-box;
}

/* body
    font-family: 'Open Sans', sans-serif */
#logo {
  width: 70px;
  height: 70px;
}

header .menu {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-align: center;
  -ms-flex-align: center;
  align-items: center;
  margin: 0px 0px;
  text-align: left;
}

header .menu a {
  margin: 0 20px;
  color: #fff;
  padding-bottom: 9px;
  display: inline-block;
  text-decoration: none;
  border-bottom: 2px solid transparent;
  font-size: 1em;
  -webkit-animation: moverIzquierda 1s ease-in;
  animation: moverIzquierda 1s ease-in;
}

header {
  background: #348f50;
  background: -webkit-gradient(
    linear,
    left top,
    right top,
    from(#56b4d3),
    to(#348f50)
  );
  background: linear-gradient(to right, #56b4d3, #348f50);
  height: auto;
  padding: 20px 48px;
  width: 100%;
}

.container2 {
  width: 95%;
  max-width: 1200px;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-align: center;
  -ms-flex-align: center;
  align-items: center;
  -ms-flex-pack: distribute;
  justify-content: space-around;
  margin: auto;
}

.portada {
  display: block;
  height: 450px;
  -o-object-fit: cover;
  object-fit: cover;
  -webkit-animation: arriba 1s ease-in;
  animation: arriba 1s ease-in;
}

.textos {
  width: 50%;
  color: #fff;
}

.textos h1 {
  font-size: 70px;
  -webkit-animation: moverDerecha 1s ease-in;
  animation: moverDerecha 1s ease-in;
}

.textos h2 {
  font-size: 30px;
  -webkit-animation: moverIzquierda 1s ease-in;
  animation: moverIzquierda 1s ease-in;
}

.textos a {
  display: inline-block;
  color: #fff;
  font-weight: 300;
  text-decoration: none;
  margin-top: 30px;
  border: 1px solid #fff;
  width: 150px;
  border-radius: 3px;
  text-align: center;
  padding: 10px 0;
  -webkit-animation: arriba 1s ease-in;
  animation: arriba 1s ease-in;
}

.wave {
  height: 100px;
  width: 100%;
  background: #348f50;
  background: -webkit-gradient(
    linear,
    left top,
    right top,
    from(#56b4d3),
    to(#348f50)
  );
  background: linear-gradient(to right, #56b4d3, #348f50);
}

@-webkit-keyframes moverIzquierda {
  0% {
    opacity: 0;
    -webkit-transform: translateX(-100px);
    transform: translateX(-100px);
  }
  100% {
    opacity: 1;
    -webkit-transform: translate(0);
    transform: translate(0);
  }
}

@keyframes moverIzquierda {
  0% {
    opacity: 0;
    -webkit-transform: translateX(-100px);
    transform: translateX(-100px);
  }
  100% {
    opacity: 1;
    -webkit-transform: translate(0);
    transform: translate(0);
  }
}

@-webkit-keyframes moverDerecha {
  0% {
    opacity: 0;
    -webkit-transform: translateX(100px);
    transform: translateX(100px);
  }
  100% {
    opacity: 1;
    -webkit-transform: translate(0);
    transform: translate(0);
  }
}

@keyframes moverDerecha {
  0% {
    opacity: 0;
    -webkit-transform: translateX(100px);
    transform: translateX(100px);
  }
  100% {
    opacity: 1;
    -webkit-transform: translate(0);
    transform: translate(0);
  }
}

@-webkit-keyframes arriba {
  0% {
    opacity: 0;
    -webkit-transform: translateY(100px);
    transform: translateY(100px);
  }
  100% {
    opacity: 1;
    -webkit-transform: translate(0);
    transform: translate(0);
  }
}

@keyframes arriba {
  0% {
    opacity: 0;
    -webkit-transform: translateY(100px);
    transform: translateY(100px);
  }
  100% {
    opacity: 1;
    -webkit-transform: translate(0);
    transform: translate(0);
  }
}
</style>