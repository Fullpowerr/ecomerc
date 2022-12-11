<template>
  <div class="display">
    <img class="picture"  :src="`/images/${imgSrc}`" />

    <div class="pictures">
      <img-id
        v-for="image in images"
        :key="image.id"
        :src="`/images/${image.src}`"
        @viewImg="replacementImage"
      />
    </div>
  </div>
</template>

<script>
export default {
  name: "product-display",

  data() {
    return {
      images: [
        { id: 1, src: "image-product-1.jpg" },
        { id: 2, src: "image-product-2.jpg" },
        { id: 3, src: "image-product-3.jpg" },
        { id: 4, src: "image-product-4.jpg" },
      ],
      imgSrc: "",
    };
  },
  methods: {
    replacementImage(image) {},
  },
};
</script>

<style scoped>
.pictures {
  display: flex;
  width: 450px;
  justify-content: space-between;
}
.picture {
  width: 450px;
  height: 450px;
  border-radius: 20px;
}
</style>
