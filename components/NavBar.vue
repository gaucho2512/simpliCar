<template>
<div> 
 <nav class="navbar navbar-expand-lg navbar-light bg-light">
  <div class="container-fluid">
    <a class="navbar-brand" href="#"><img class="logo-nissan" src="../assets/image/logo.jpg" alt="logo"></a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto mb-2 mr-auto nav-btn">
        <li class="nav-item">
          <nuxt-link class="nav-link"  to="/">Home</nuxt-link>
        </li>
        <li class="nav-item">
           <nuxt-link class="nav-link"  to="/productos">Vehículos</nuxt-link>
        </li>
      </ul>
      <form class="d-flex">
        <input class="form-control me-2" type="search" placeholder="Buscar Vehículo" aria-label="Search">
        <button class="btn btn-outline-primary" type="submit">Buscar</button>
      </form>
    </div>
  </div>
</nav>
</div>
</template>

<script>
export default {

}
</script>

<style>
.logo-nissan{
    width: 16%;
}
.nav-btn{
   font-size: 22px;
   margin-right: 150px;
}
.nav-link{
  color: black;

}  
</style>