<template lang="html">

<div class="">
  <section class="menu-barra-itas" id="menu-barra-itas">
  <div class="img-menu">
  <a href="#"> <img src="../assets/itas-logo-alt.png" alt="" width="200px"></a>
  </div>
  <div class="btn-hamburguesa">
    <a href="#" id="btn-abrirmenu" v-on:click="abrirMenu" >A</a>
    <a href="#" id="btn-cerrarmenu" v-on:click="cerrarMenu" >X</a>
  </div>

</section>
<nav class="itasmenu" id="itasmenu">

<section class="contenedorelemento">
<section class="cont-img-menu">
<a href="#"> <img src="../assets/itas-logo-alt.png" alt="" width="200px" title="Inéditas Films"></a>
</section>

<section class="cont-menu-itas">
  <ul id="subcont-menu-itas">
<li><a href="#" id="nosotros" title="Nosotros">Nosotros</a></li>
<li id="inedito"><a href="" title="Lo inédito">Lo inédito</a>
                <ul id="submenu-itas">
                  <li><a href="" title="Fotografías">Fotografías</a></li>
                  <li><a href="" title="Documentales">Documentales</a></li>
                </ul>
          </li>
<li><a href="#" title="Servicios">Servicios</a></li>
<li><a href="#" title="Contacto">Iniciar sesión</a></li>
  </ul>
  </section>
</section>


</nav>
<div class="caja-menu"></div>
</div>

</template>

<script>
export default {
  methods: {
  abrirMenu:  function (){
  var elemento = document.getElementById('subcont-menu-itas');
  var abrir = document.getElementById('btn-abrirmenu');
  var cerrar = document.getElementById('btn-cerrarmenu');
  elemento.style.transition = "max-height 0.3s ease-in";
  elemento.style.maxHeight = "800px";
  abrir.style.display = "none";
  cerrar.style.display = "block";
},

  cerrarMenu: function (){
  var elemento = document.getElementById('subcont-menu-itas');
  var abrir = document.getElementById('btn-abrirmenu');
  var cerrar = document.getElementById('btn-cerrarmenu');
  elemento.style.transition = "max-height 0.3s";
  elemento.style.maxHeight = "0px";
  abrir.style.display = "block";
  cerrar.style.display = "none";
}
},
mounted(){
  window.onresize = function(){
  var elemento = document.getElementById('subcont-menu-itas');
  var abrir = document.getElementById('btn-abrirmenu');
  var cerrar = document.getElementById('btn-cerrarmenu');
  var anchoPantalla = window.innerWidth;
  var video = document.getElementById('video');
  var boton = document.getElementById('btn-vol');
  var ancho = window.innerWidth;
  if(anchoPantalla > 800){
    elemento.style.maxHeight = "800px";
    abrir.style.display = "block";
    cerrar.style.display = "none";
  }else{
    elemento.style.maxHeight = "0px";
    abrir.style.display = "block";
    cerrar.style.display = "none";

  }
  }
}



}
</script>

<style lang="css">




/*----------------BARRARESPONSIVE-------------*/
.menu-barra-itas{
  width:100%;
  background:black;
  padding:10px;
  display: none;
}
.menu-barra-itas .btn-hamburguesa{
  display: -webkit-flex;
  display: -ms-flex;
  display: flex;
}
.menu-barra-itas a{
  padding:8px;
  background:black;
  color:white;
  text-decoration:none;
}
#btn-cerrarmenu{
  display: none;
  font-size:1.2em;
  cursor:pointer;
}
#btn-abrirmenu{
  font-size:1.2em;
  cursor:pointer;
}
.img-menu{

}
.img-menu img{
}
/*----------------BARRARESPONSIVE-------------*/
/*---------------------MENU--------------------*/

.itasmenu{
  width:100%;
  background:black;
  display: -webkit-flex;
  display: -ms-flex;
  display: flex;
  flex-flow:row wrap;
  justify-content: center;
  align-items: center;
  position: fixed;
  z-index:10;
  top:0px;
}
.contenedorelemento{
  width:100%;
  max-width:1400px;
  background:black;
  padding:0px 10px;
  display: -webkit-flex;
  display: -ms-flex;
  display: flex;
  flex-flow:row wrap;
  justify-content: space-between;
  align-items: center;
}
.cont-menu-itas{
  background:black;
  padding:10px;
  display: -webkit-flex;
  display: -ms-flex;
  display: flex;
}
.cont-menu-itas ul{
  background:pink;
  list-style: none;
  display: -webkit-flex;
  display: -ms-flex;
  display: flex;
  flex-flow:row wrap;
}
.cont-menu-itas >ul >li{
  background:brown;
  display: -webkit-flex;
  display: -ms-flex;
  display: flex;
  position:relative;
}
.cont-menu-itas >ul >li >a{
  padding:10px 20px;
  background:black;
  color:white;
  text-decoration:none;
  position:relative;
}
.cont-menu-itas >ul >li>a:before{
  content: "";
  width:100%;
  height:100%;
  border:2px solid rgba(94,139,111,0);
  display: -webkit-flex;
  display: -ms-flex;
  display: flex;
  position:absolute;
  z-index:20;
  top:0;
  left:0;

}
.cont-menu-itas >ul >li >a:hover:before{
  border:2px solid rgba(94,139,111,1);
}
.cont-menu-itas >ul{
  display: -webkit-flex;
  display: -ms-flex;
  display: flex;
  align-items: center;
}
.cont-menu-itas >ul >li >ul{
  background:green;
  max-height:0px;
  padding:0px;
  display: -webkit-flex;
  display: -ms-flex;
  display: flex;
  flex-flow:column;
  position:absolute;
  z-index:19;
  top:100%;
  left:0px;
  overflow:hidden;
  -webkit-transition: all 0.5s;
  -o-transition: all 0.5s;
  transition: all 0.5s;
}
.cont-menu-itas >ul >li >ul >li{
  display: -webkit-flex;
  display: -ms-flex;
  display: flex;
  flex-flow:row wrap;
  padding:0px;
}
.cont-menu-itas >ul >li >ul a{
  width:100%;
  color:white;
  padding:20px 20px;
  text-decoration:none;
  background:black;
}
.cont-menu-itas >ul >li >ul a:hover{
  color:#5e8b6f;
}
#inedito:hover #submenu-itas{
  max-height:500px;
}
.caja-menu{
  width:100%;
  max-width:1400px;
  height:59px;
  background:#ccc;
}

/*---------------------MENU--------------------*/

@media screen and (max-width:800px) {
  /*---------------------MENU--------------------*/
  .itasmenu{
    padding:0px;
    top:59px;
    left:0px;
  }
  .cont-img-menu{
    display:none;
  }
  .cont-menu-itas{
    width:100%;
    padding:0px;
  }
  .cont-menu-itas ul{
    flex-flow:column;
    width:100%;
  }
  .cont-menu-itas ul>li{
    width:100%;
  }
  .cont-menu-itas ul>li>a{
    width:100%;
  }
  .cont-menu-itas >ul >li >ul{
    position: relative;
    top:0px;
  }
  .cont-menu-itas >ul >li >ul a{
    background:#1e1c1c;
  }
  .cont-menu-itas >ul >li >ul a:hover{
    color:white;
    background:#161414;
  }
  #inedito{
    width:100%;
    display: -webkit-flex;
    display: -ms-flex;
    display: flex;
    flex-flow:column;
  }
  #nosotros{
    border:none;
  }
  #subcont-menu-itas{
    position: absolute;
    max-height:0px;
    overflow:hidden;
    z-index:21;
    left:0px;
  }
  .menu-barra-itas{
    display: -webkit-flex;
    display: -ms-flex;
    display: flex;
    flex-flow:row wrap;
    justify-content: space-between;
    align-items: center;
    position:fixed;
    top:0px;
    z-index:11;
  }
  .cont-menu-itas >ul >li >a:before{
    border:none;
  }
  .cont-menu-itas >ul >li >a:hover{
    color:#5e8b6f;
  }
  .cont-menu-itas >ul >li >a:hover:before{
    border:none;
  }
  /*---------------------MENU--------------------*/
}







</style>
