<template>
  <div class="card my-2 item-todo">
    <h5>{{ tache }}</h5>
    <div @click="suppression" class="button-supr btn btn-danger">X</div>
  </div>
</template>

<script>
export default {
  name: "item-vue",
  props: ["tache", "suppression"],
};
</script>

<style scoped>
.item-todo {
  position: relative;
  padding: 20px 60px 20px 30px;
  font-size: 20px;
  height: 88px;
}
.button-supr {
  position: absolute;
  top: 10px;
  right: 10px;
}
.item-todo h5 {
  margin-bottom: 0 !important;
}
</style>