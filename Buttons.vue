<template>
    <button class="btn">
      <slot></slot>
    </button>

</template>

<script>
export default {
  name: "my-buttons",
};
</script>

<style scoped>

.btn {
  width: 280px;
  height: 48px;
  background-color: hsl(26, 100%, 55%);
  border-radius: 12px;
  border: none;
  color: white;
  font-family: "Kumbh Sans", sans-serif;
  font-size: 20px;
  align-items: center;
  display: flex;
  justify-content: center;
}
button:hover {
  opacity: 0.65;
}

</style>
