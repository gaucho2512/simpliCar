<template>
  <div class="container">
     <div class="card">
         <div class="card-body">
             <h1>{{ articulo.title }}</h1>
             <p>{{ articulo.body }}</p>
             <nuxt-link to="/productos" class="btn btn-primary">atras</nuxt-link>
            
         </div>
     </div>
  </div>
</template>

<script>
import axios from "axios"

export default {
    data() {
        return {
          articulo: null
        }
    },

    // se puede hacer de las dos formas , solo que con created si llamas a dos o mas peticiones puede llegar a tardar mucho, //

    /*  async created() { 
     try { const res = await axios.get(`https://jsonplaceholder.typicode.com/posts/${this.$route.params.id}`)
         this.articulo = res.data
        
    } catch (error) {
        console.log(error)
        
    }    */
            
     

     async asyncData({params , route , res , store , error}) {
         try {  const res = await axios.get(`https://jsonplaceholder.typicode.com/posts/${params.id}`)
         const articulo = res.data
            return {articulo}
             
         } catch (error) {
             console.log(error)
              return {error : error}
         }
     }

}
</script>

<style>

</style>