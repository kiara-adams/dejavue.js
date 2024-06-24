<template>
  <div>
    <h2>Cars</h2>
    <div class="card-list">
      <slot name="cars"></slot>
    </div>

    <h2>Gaming Consoles</h2>
    <div class="card-list">
      <slot name="consoles"></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CardComp',
};
</script>

<style scoped>
.card-list {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
  gap: 20px;
}


</style>
