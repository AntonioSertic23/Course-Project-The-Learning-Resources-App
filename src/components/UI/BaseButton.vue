<template>
  <button :class="mode">
    <slot></slot>
  </button>
</template>

<script>
export default {
  props: ['mode'],
};
</script>

<style scoped>
button {
  padding: 0.75rem 1.5rem;
  font-family: inherit;
  background-color: #5e548e;
  border: 1px solid #5e548e;
  color: white;
  cursor: pointer;
}

button:hover,
button:active {
  background-color: #231942;
  border-color: #231942;
}

.flat {
  background-color: transparent;
  color: #5e548e;
  border: none;
}

.flat:hover,
.flat:active {
  background-color: #cdb4db;
}
</style>
