<template>
  <div class="container mt-5">
    <h1 style="textalign: center">Rentrez les tâches à faire.</h1>
    <form>
      <div class="form-group">
        <label for="action">Action</label>
        <input
          v-model="formData.tache"
          type="text"
          id="action"
          class="form-control"
        />
      </div>
      <button @click.prevent="createTache" class="btn btn-primary mt-4 mb-4">
        Créer une tâche
      </button>
    </form>

    <ul>
      <li v-bind:key="index" v-for="(tache, index) in tacheTable">
        <item-vue
          v-bind:key="index"
          :tache="tache"
          :suppression="() => suppression(index)"
        ></item-vue>
      </li>
    </ul>
  </div>
</template>


<script>
import Item from "./Item";
export default {
  name: "tache-a-faire",
  data() {
    return {
      formData: {
        tache: "",
      },
      tacheTable: ["React", "Vue", "Javascript", "Tailwind"],
    };
  },
  components: {
    "item-vue": Item,
  },
  methods: {
    createTache: function () {
      this.tacheTable.push(this.formData.tache);
      this.formData.tache = "";
    },
    suppression: function (index) {
      this.tacheTable.splice(index, 1);
    },
  },
};
</script>


<style scoped>
ul {
  list-style-type: none;
  padding: 0;
}
</style>