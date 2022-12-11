<template>
  <div class="basket" v-if="view" @click.stop="viewClick">
    <div class="card-item"><strong>Shopping cart</strong></div>
    <div class="card-item">
      <img
        src="/images/image-product-1-thumbnail.jpg"
        width="60"
        height="60"
        alt="image"
      />
      <p>Fall Limited Edition Sneakers $125.00 <strong>x</strong></p>
      <svg
        width="16"
        height="18"
        xmlns="http://www.w3.org/2000/svg"
        xmlns:xlink="http://www.w3.org/1999/xlink"
      >
        <defs>
          <path
            d="M0 2.625V1.75C0 1.334.334 1 .75 1h3.5l.294-.584A.741.741 0 0 1 5.213 0h3.571a.75.75 0 0 1 .672.416L9.75 1h3.5c.416 0 .75.334.75.75v.875a.376.376 0 0 1-.375.375H.375A.376.376 0 0 1 0 2.625Zm13 1.75V14.5a1.5 1.5 0 0 1-1.5 1.5h-9A1.5 1.5 0 0 1 1 14.5V4.375C1 4.169 1.169 4 1.375 4h11.25c.206 0 .375.169.375.375ZM4.5 6.5c0-.275-.225-.5-.5-.5s-.5.225-.5.5v7c0 .275.225.5.5.5s.5-.225.5-.5v-7Zm3 0c0-.275-.225-.5-.5-.5s-.5.225-.5.5v7c0 .275.225.5.5.5s.5-.225.5-.5v-7Zm3 0c0-.275-.225-.5-.5-.5s-.5.225-.5.5v7c0 .275.225.5.5.5s.5-.225.5-.5v-7Z"
            id="a"
          />
        </defs>
        <use fill="#C3CAD9" fill-rule="nonzero" xlink:href="#a" />
      </svg>
    </div>

    <my-buttons style="margin: auto"> Chekout</my-buttons>
  </div>
</template>

<script>
export default {
  name: "basket-window",
  props: {
    view: {
      type: Boolean,
      required: false,
    },
  },
  methods: {
    viewClick() {
      this.$emit("update:view", false);
    },
  },
};
</script>

<style scoped>
.basket {
  font-family: "Kumbh Sans", sans-serif;
  position: absolute;
  margin-top: 55px;
  right: 15%;
  width: min(360px, 95%);
  width: 360px;
  height: 220px;
  box-shadow: 0 20px 50px -20px #1d202680;
  background-color: #fff;
  justify-content: center;
  border-radius: 30px;
}
.card-item {
  display: flex;
  text-align: start;

  justify-content: center;
  align-items: center;
  margin: 15px;
}
img {
  margin: 10px;
  border-radius: 5px;
}
p {
  color: gray;
  line-height: 25px;
}
* {
  margin-top: -3%;
}
</style>
