<template>
<div>
  <div class="row productos" >
    <div class="col-md-12">
      <h2 class="title-productos">¿CÁUL VA A SER TU PROXIMO NISSAN?</h2>
    </div>

    <button></button>
    <button></button>
    <button></button>
  </div>
  <div class="row card-productos">
    <img src="..." class="card-img-top" alt="...">
    <div class="col-md-3 card my-4 ml-5" v-for="(item , index) in articulos" :key="index">
      <div class="card-body">
          <nuxt-link :to="`productos/${item.id}`">
              <h3>{{ item.title }}</h3>
              <p> {{item.body}}</p>
              <a href="#" class="btn btn-primary">VER</a>
        </nuxt-link>
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


     async created() {

         try {
        const res = await axios.get("https://jsonplaceholder.typicode.com/posts?_limit=10")
        console.log(res.data)
        this.articulos = res.data
    } catch (error) {
                console.log(error)
    
}
    
}
   
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
  height: 1000px;
}



</style>