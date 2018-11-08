<template lang="html">
  <div class="contenedor-f">
<footer class="footer-itas">
<section class="foot-terminos-itas">
              <p>©2018 Inéditas films Terms and conditions Legal</p>
          </section>

<section class="foot-btns-itas">
                  <div class="foot-btn-registro-itas">
                    <a href="#" title="Registrate">Registrarse</a>
                    <a href="#" title="Iniciar sesión">Iniciar sesión</a>
                  </div>
                  <div class="foot-btn-redes-itas">
                    <a href="https://www.facebook.com/ineditasfilmsmx/" target="_blank" class="icon-facebook" title="Ir a facebook"></a>
                    <a href="mailto:ineditas@inbox.com" class="icon-mail3" title="Enviar correo"></a>
                    <a href="https://vimeo.com/user1518493" target="_blank" class="icon-vimeo3" title="Ver en vimeo"></a>
                  </div>
        </section>
</footer>
  </div>
</template>

<script>
export default {
}
</script>

<style lang="css">
/*-------------------------FOOTER--------------*/
.contenedor-f{
  width:100%;
  background:black;
  display:flex;
  justify-content: center;
}
.footer-itas{
  width:100%;
  max-width:1400px;
  background:black;
  display: -webkit-flex;
  display: -ms-flex;
  display: flex;
  flex-flow:column;
  -webkit-transition: all 0.5s;
  -o-transition: all 0.5s;
  transition: all 0.5s;
}
.foot-terminos-itas{
  width:100%;
  text-align: center;
  padding:20px;
  color:white;
  -webkit-transition: all 0.5s;
  -o-transition: all 0.5s;
  transition: all 0.5s;
}
.foot-terminos-itas p{

}
.foot-btns-itas{
  width:100%;
  display: -webkit-flex;
  display: -ms-flex;
  display: flex;
  flex-flow:row wrap;
  justify-content: space-between;
  align-items:center;
  padding:20px;

  -webkit-transition: all 0.5s;
  -o-transition: all 0.5s;
  transition: all 0.5s;
}
.foot-btn-registro-itas{
  display: -webkit-flex;
  display: -ms-flex;
  display: flex;
  -webkit-transition: all 0.5s;
  -o-transition: all 0.5s;
  transition: all 0.5s;
}
.foot-btn-registro-itas a{
  padding:10px;
  margin:5px;
  background:#5e8b6f;
  text-decoration: none;
  color:white;
  font-size:0.8em;
  -webkit-transition: all 0.2s;
  -o-transition: all 0.2s;
  transition: all 0.2s;
}
.foot-btn-registro-itas a:hover{
  background:#496853;
}
.foot-btn-redes-itas{
  display: -webkit-flex;
  display: -ms-flex;
  display: flex;
  -webkit-transition: all 0.5s;
  -o-transition: all 0.5s;
  transition: all 0.5s;
}
.foot-btn-redes-itas a{
  width:30px;
  height:30px;
  margin:5px;
  color:#5e8b6f;
  text-align: center;
  line-height:30px;
  background:white;
  text-decoration:none;
}
/*-------------------------FOOTER--------------*/
@media screen and (max-width:500px){
  .foot-btns-itas{
    display: -webkit-flex;
    display: -ms-flex;
    display: flex;
    flex-flow:column;
    padding:10px;
  }
  .foot-terminos-itas{
    padding:10px 20px;
  }
  .foot-terminos-itas p{
    font-size:0.8em;
  }
  .foot-btn-registro-itas a{
    margin:0px 5px 10px 5px;
  }
}
</style>
