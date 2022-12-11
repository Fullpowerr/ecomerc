<template>
  <div class="footer">
    <div class="navBar">
      <img src="/images/SNEAKERS.svg" alt="Логотип" />
      <div class="links">
        <a href="">Collections</a>
        <a href="">Men</a>
        <a href="">Woomen</a>
        <a href="">About</a>
        <a href="">Contact</a>
      </div>

      <div class="basket">
        <button class="btn" @click="clickView">
          <svg width="22" height="20" xmlns="http://www.w3.org/2000/svg">
            <path
              d="M20.925 3.641H3.863L3.61.816A.896.896 0 0 0 2.717 0H.897a.896.896 0 1 0 0 1.792h1l1.031 11.483c.073.828.52 1.726 1.291 2.336C2.83 17.385 4.099 20 6.359 20c1.875 0 3.197-1.87 2.554-3.642h4.905c-.642 1.77.677 3.642 2.555 3.642a2.72 2.72 0 0 0 2.717-2.717 2.72 2.72 0 0 0-2.717-2.717H6.365c-.681 0-1.274-.41-1.53-1.009l14.321-.842a.896.896 0 0 0 .817-.677l1.821-7.283a.897.897 0 0 0-.87-1.114ZM6.358 18.208a.926.926 0 0 1 0-1.85.926.926 0 0 1 0 1.85Zm10.015 0a.926.926 0 0 1 0-1.85.926.926 0 0 1 0 1.85Zm2.021-7.243-13.8.81-.57-6.341h15.753l-1.383 5.53Z"
              fill="#69707D"
              fill-rule="nonzero"
            />
          </svg>
        </button>

        <img
          class="autor"
          src="/images/autor.jpeg"
          alt="Фото автора"
          width="15%"
        />
      </div>
    </div>
    <basket-window v-model:view="visible" />
  </div>
</template>

<script>
export default {
  name: "Myfooter",
  data() {
    return {
      visible: false,
    };
  },
  methods: {
    clickView() {
      this.visible = true;
    },
    closeModal() {
      this.visible = false;
    },
  },
};
</script>
<style scoped>
.btn {
  border: none;
}
.navBar {
  display: flex;
  margin: 50px;
  justify-content: space-between;
  text-align: center;
  align-items: center;
  font-family: "Kumbh Sans", sans-serif;
}
a {
  padding-left: 25px;
  text-decoration: none;
  color: gray;
}
.autor {
  margin-left: 30px;
}
.links {
  margin-right: 25em;
}
</style>
