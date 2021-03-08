<template>
  <div class="fondo-home">
    <div class="row">
      <div class="col-md-6">
        <div>
          <h1 class="titulo-home">AHORA ES ONLINE</h1>
          <p class="parrafo-home">
            Con Nissan Store, podés acceder a tu nuevo 0Km con todos los
            servícios asociados desde la comodidad de tu sofá. 
            Probanos!
          </p>
          <a href="https://www.nissan.com.ar/" target="_blank" class="btn btn-danger btn-lg btn-home"> INGRESAR A NISSAN STORE </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style >
.fondo-home {
  background-image: url(../assets/image/fondo3.jpg);
  max-width: 100%;
  height: 1080px;
 
}
.titulo-home{
  color: #e40017;
  margin-top: 100px;
  margin-left: 50px;
  font-size: 60px;
  padding: 30px;
  font-weight: bold;
}
.parrafo-home{
  font-size: 22px;
  margin-left: 80px;
   font-weight: 600;
}
.btn-home{
  margin-top: 40px;
  margin-left: 80px;
}
</style>
