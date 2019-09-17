<template>
    <div><header>
        <div id="nav" class="container-fluid">
            <nav class="navegacion nav">
                <a class="" href="index.html"><img id="logo" src="@/assets/logo.png" alt="Logo"></a>
                <a class="" href="@/BronsCategories.vue">EXPLORE</a>
                <a class="" href="#">ADD A LISTING</a>
            </nav>
        </div>
    </header>                                                                          
    </div>
</template>
<style scoped>
#nav {
  position: fixed;
  padding: 0px;
  z-index: 1;
}

#nav .navegacion {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-align: center;
      -ms-flex-align: center;
          align-items: center;
  background: #F2F2F2;
  padding: 0px 20px;
}

#nav .navegacion a {
  padding: 0px 15px;
  color: #585858;
  text-decoration: none;
  font-size: 1rem;
}

#nav .navegacion a:hover {
  color: #000;
}

#nav .navegacion a:focus {
  color: red;
}

#logo {
  width: 70px;
}
</style>