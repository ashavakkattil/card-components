<template>
  <div>
    <q-card
      class="coffee-card"
      flat
      bordered
      @mouseenter="addPadding = true"
      @mouseleave="addPadding= false"
      :class="addPadding ? 'bg-brown-10': ''"
    >
      <q-img
        :class="addPadding ? 'card-zoom-out': 'card-zoom-in'"
        src="https://cdn.shopify.com/s/files/1/0849/4852/t/3/assets/custom_showcase1_img.jpg?v=13773551431648647157"
      ></q-img>
      <q-card-section class="text-center">
        <div class="text-h4 text-weight-bold text-white">Elite Coffee</div>
        <div class="text-h6 text-brown-4 text-uppercase">Get upto 30% off</div>
      </q-card-section>
      <div class="cart-icon">
        <q-icon name="mdi-cart" size="lg" class="cart"></q-icon>
      </div>
    </q-card>
  </div>
</template>
<script>
export default {
  data() {
    return {
      addPadding: false
    };
  }
};
</script>
<style lang="scss" scoped>
.coffee-card {
  width: 300px;
  background-color: #96ca2d;
  border-radius: 10px;
}
.card-zoom-out {
  transform: scale(0.93);
  transition: 0.6s ease-in-out;
}
.card-zoom-in {
  transition: 0.6s ease-in-out;
}
.cart-icon {
  position: relative;
  width: 80px;
  height: 70px;
  background: grey;
  top: 30px;
  left: 38%;
  border-radius: 10px !important;
  text-align: center;
  .cart {
    position: relative;
    top: 15px;
    color: white;
  }
}
</style>
