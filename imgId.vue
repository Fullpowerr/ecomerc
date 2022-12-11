<template>
  <img class="img" alt="image" 
  @click ="$emit('viewImg', image)"
  />
</template>

<script>
export default {
  name: "img-id",
  
  data() {
    return {
      image:{id:'', src:''}
    };
  },
  methods: {},
};
</script>

<style scoped>
.img {
  width: 86px;
  height: 86px;
  margin: 10px;
  border-radius: 5px;
  margin: auto;

}
img.animation:hover {
  opacity: 0.45;
}
</style>
