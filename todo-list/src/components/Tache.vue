<template>
   <div class="container mt-5">
    <h1 style="textAlign:center">Rentrez les tâches à faire. </h1>
    <form >
    <div class="form-group">
  <label for="action">Action</label>
  <input type="text" id="action" class="form-control">
    </div>
    <button class="btn btn-primary mt-4" >Créer une tâche </button>

    </form>
  
    <ul>
        <li v-bind:key="index" v-for="(tache,index) in tacheTable">
        <item-vue :tache="tache" :suppression="suppression"></item-vue>
        </li>
    </ul>

   </div>
</template>


<script>
import Item from './Item'
export default{
    name: 'tache-a-faire',
    data() {
        return{
          formData:{
            tache:"",
          },
          tacheTable:['React','Vue','Javascript','Tailwind']
          
        }
        
    },
    components:{
        'item-vue': Item
    }
    
}

</script>


<style scoped>
ul{
    list-style-type: none;
}
</style>