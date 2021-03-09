 <template>
 <div>
  <div class="row productos" >
    <div class="col-sm-12 col-md-12 col-lg-12">
      <h2 class="title-productos">¿CUÁL VA A SER TU PROXIMO NISSAN?</h2>
    </div>
     </div>

     <div class="btn-dropdown">
       <div>
  <b-dropdown id="dropdown-1" text="CARROCERIA" class="m-md-2">
    <b-dropdown-item>Usados</b-dropdown-item>
    <b-dropdown-item>Nuevos</b-dropdown-item>
    <b-dropdown-item>Coleccion</b-dropdown-item>
  </b-dropdown>
</div>

<div>
  <b-dropdown id="dropdown-2" text="MODELO" class="m-md-2">
    <b-dropdown-item>2019</b-dropdown-item>
    <b-dropdown-item>2020</b-dropdown-item>
    <b-dropdown-item>2021</b-dropdown-item>
  </b-dropdown>
</div>

<div>
  <b-dropdown id="dropdown-3" text="PRECIO" class="m-md-2">
    <b-dropdown-item>Hasta $500.000</b-dropdown-item>
    <b-dropdown-item>Hasta $1.000.000</b-dropdown-item>
    <b-dropdown-item>Mas de $1.000.000</b-dropdown-item>
  </b-dropdown>
</div>
     </div>
 
  <div class="body-productos">
  <div class="row card-productos">
    <div class="col-sm-3 col-md-3 col-lg-3 card my-4 ml-5" v-for="(item , index) in articulos" :key="index">
      <img :src="item.gallery[2].large" alt="">
    
           
 
      <div class="card-body">
         
              <h3>{{ item.model }}</h3>
              <p> PRECIO DESDE :  {{item.amount}}</p>
            
       <nuxt-link :to="`productos/${item.id}`" class="btn btn-danger"> VER DETALLES DEL MODELO  </nuxt-link>

      </div>
    </div>
  </div>
  </div> 
  </div>
</template>

<script>

 import axios from "axios"
export default {
    data() {
        return {
            articulos: [],    
        }
    },


/* LLAMADA A LA API CON AXIOS */
  async created() {
  const res = await axios.get("https://4my1q6hsyo.api.quickmocker.com/product", {
    method:"GET",
    headers: {
      "Content-Type" : "application/json",
      Authorization: "Bearer" + "qwertyuiopasdfghjklzxcvbnm123456" 
    },
  })
  console.log(res.data.results)
  this.articulos = res.data.results
} ,

 
};  
</script>

  <style scoped>
 .title-productos{
  color: white;
  font-size: 36px;
  font-weight: bold;
  background-color: #92967d;
  height: 110px;
  text-align: center;
  padding-top: 25px;
}
.card-productos{
  width: 100%;
  height: 900px;
} 
.btn-dropdown{
  display: flex;
  margin-left: 33px;
  height: 80px;
}
.body-productos{
  height: 1700px;
}



</style>   