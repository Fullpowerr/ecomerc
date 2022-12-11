<template>
    <div class="cardInfo">
  <div class="text">
    <h3 class="mr">SNEAKERS COMPANY</h3>
    <h1 lass="mr"><strong>Fall Limited Edition <br> Sneakers</strong></h1>
    <p lass="mr"> These low-profile sneakers are your perfect casual wear <br> companion. Featuring a durable rubber outer sole, they’ll <br> withstand everything the weather can offer.</p>
  </div>
  <div class="price">
    <div class="flex">
    <h2 lass="mr"><strong>$125.00</strong></h2> <h3 class="discount">50%</h3>
  </div>
    <div class="blacked mr"><del>$250.00</del></div>
  </div>
 
  <div class="count">
      <svg
        @click="countMinus"
        width="12"
        height="4"
        xmlns="http://www.w3.org/2000/svg"
        xmlns:xlink="http://www.w3.org/1999/xlink"
      >
        <defs>
          <path
            d="M11.357 3.332A.641.641 0 0 0 12 2.69V.643A.641.641 0 0 0 11.357 0H.643A.641.641 0 0 0 0 .643v2.046c0 .357.287.643.643.643h10.714Z"
            id="a"
          />
        </defs>
        <use fill="#FF7E1B" fill-rule="nonzero" xlink:href="#a" />
      </svg>
      <div @count="countSave">
        <h2>{{ counter }}</h2>
        
      </div>
      <svg
        @click="countPlus"
        width="15"
        height="15"
        xmlns="http://www.w3.org/2000/svg"
        xmlns:xlink="http://www.w3.org/1999/xlink"
      >
        <defs>
          <path
            d="M12 7.023V4.977a.641.641 0 0 0-.643-.643h-3.69V.643A.641.641 0 0 0 7.022 0H4.977a.641.641 0 0 0-.643.643v3.69H.643A.641.641 0 0 0 0 4.978v2.046c0 .356.287.643.643.643h3.69v3.691c0 .356.288.643.644.643h2.046a.641.641 0 0 0 .643-.643v-3.69h3.691A.641.641 0 0 0 12 7.022Z"
            id="b"
          />
        </defs>
        <use fill="#FF7E1B" fill-rule="nonzero" xlink:href="#b" />
      </svg>
      <my-buttons> 
          <svg  style="margin-left: -5px" width="22" height="20" xmlns="http://www.w3.org/2000/svg">
        <path
          d="M20.925 3.641H3.863L3.61.816A.896.896 0 0 0 2.717 0H.897a.896.896 0 1 0 0 1.792h1l1.031 11.483c.073.828.52 1.726 1.291 2.336C2.83 17.385 4.099 20 6.359 20c1.875 0 3.197-1.87 2.554-3.642h4.905c-.642 1.77.677 3.642 2.555 3.642a2.72 2.72 0 0 0 2.717-2.717 2.72 2.72 0 0 0-2.717-2.717H6.365c-.681 0-1.274-.41-1.53-1.009l14.321-.842a.896.896 0 0 0 .817-.677l1.821-7.283a.897.897 0 0 0-.87-1.114ZM6.358 18.208a.926.926 0 0 1 0-1.85.926.926 0 0 1 0 1.85Zm10.015 0a.926.926 0 0 1 0-1.85.926.926 0 0 1 0 1.85Zm2.021-7.243-13.8.81-.57-6.341h15.753l-1.383 5.53Z"
          fill="#ffff"
          fill-rule="nonzero"
        />
      </svg>Add to Cart
        </my-buttons>
    </div>
    
</div>
</template>

<script>
export default {
name: 'product-info',
data() {
    return {
      counter: 0,
    };
  },
methods: {
    countPlus(counter) {
      this.counter++;
    },
    countMinus(counter) {
      if (this.counter === 0) {
        this.counter = 0;
      } else {
        this.counter--;
      }
    }
  },
  countSave(counter){
    this.$emit('getNumber', this.counter)
  }
}
</script>

<style scoped>
.cardInfo {
width: 458px;
height: 573px;
margin: auto;
line-height: 35px;
font-family: 'Kumbh Sans', sans-serif;
}
h3 {
    color: hsl(26, 100%, 55%);
    margin-bottom: 20px;
    letter-spacing : 5px;
    font-size: 15px;
}
p{
    color:  hsl(0, 0%, 43%);
    font-size: 16px;
    margin-bottom: 20px;
}
.count {
  align-items: center;
  display: flex;
}
h1 {
  margin-bottom: 20px;
  font-size: 45px;
  line-height: 45px;

}
.text {
  margin-top: 70px;
}
.blacked {
  color:  hsl(0, 4%, 76%);
}
.price {
  font-size: 20px;
}
.discount {
  color:  hsl(26, 100%, 55%);
  margin-left: 40px;
}
.flex {
  display: flex;
}
svg {
  margin: 0px 35px 0px 35px;
  cursor: pointer;
}


</style>