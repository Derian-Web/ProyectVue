<template>
    <div>
        <footer>
        <div>
            <span>Do you like Eco-Awarenes?</span>
            <span class="orange">Advertise with us</span>
        </div>
        <div id="developers">
            <div>Developed By:&nbsp;</div>
            <div class="orange">Ricardo <br>Salvador <br>Reywis</div>
        </div>
    </footer>
    </div>
</template>
 <style  scoped>
 footer {
  background: #F2F2F2;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-pack: justify;
      -ms-flex-pack: justify;
          justify-content: space-between;
  padding: 20px;
  font-size: .8rem;
  color: #585858;
}

.orange {
  color: #FE9A2E;
}

#developers {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  min-width: 100px;
}

#developers div {
  display: inline-block;
  min-width: 10px;
}
 </style>