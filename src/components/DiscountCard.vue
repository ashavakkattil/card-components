<template>
  <div class="row justify-center">
    <q-card class="my-card" flat bordered>
      <q-img
        :src="showImage?'https://cdn.shopify.com/s/files/1/0815/1651/products/florida_eco_safari_1_large.jpeg?v=1427723864': 'https://cdn.shopify.com/s/files/1/0815/1651/products/florida_eco_safari_2_large.jpeg?v=1427723864'"
        @mouseleave="showImage = true"
        @mouseenter="showImage = false"
      >
        <div class="product-badge">
          <span class="text-uppercase">new</span>
        </div>

        <div class="add-to-cart-btn" v-show="!showImage">
          <transition
            appear
            enter-active-class="animated fadeInDown"
            leave-active-class="animated fadeInUp"
          >
            <q-btn text color="primary">Add to cart</q-btn>
          </transition>
        </div>
      </q-img>
      <q-card-section class="text-center">
        <div class="text-h6">Florida Eco Safari</div>
        <div
          class="text-subtitle1 card-text"
        >This is Florida eco safari.Of course you can rely on your GPS system</div>
        <div class="q-mt-md">
          <span class="text-h6 text-teal q-mr-md">$410.00</span>
          <span class="text-h6 text-teal-3 q-mr-md old-price">$500.00</span>
        </div>
      </q-card-section>
    </q-card>
  </div>
</template>
<script>
export default {
  data() {
    return {
      showImage: true
    };
  }
};
</script>
<style lang="scss" scoped>
.my-card {
  width: 300px;
  .card-text {
    line-height: 1.2em;
    color: grey;
  }
}

.old-price {
  text-decoration: line-through;
}
.product-badge {
  padding: 5px;
  width: 156px;
  text-align: center;
  transform: rotate(-45deg);
  position: relative;
  left: -45px;
  top: 30px;
  background-color: #11bf8a;
}
.add-to-cart-btn {
  position: absolute;
  top: 40%;
  left: 25%;
  background-color: transparent;
}
</style>
