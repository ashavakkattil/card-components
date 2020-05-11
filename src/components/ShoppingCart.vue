<template>
  <div>
    <q-card class="shopping-card" flat>
      <div class="cart-image q-mb-lg">
        <q-img
          @mouseenter="showImage = false"
          @mouseleave="showImage= true"
          :src="showImage? 'https://cdn.shopify.com/s/files/1/0849/4852/products/keurig_caribou_coffee_caribou_blend_k-cup_packs_72-count_1_large.png?v=1430308503': 'https://cdn.shopify.com/s/files/1/0849/4852/products/keurig_caribou_coffee_caribou_blend_k-cup_packs_72-count_2_large.png?v=1430308503'"
        ></q-img>
      </div>

      <q-card-section>
        <div class="text-h4 text-weight-bold text-accent">$ 26.00</div>
        <div class="text-uppercase q-my-md">Keurig Caribou Coffee ...</div>
        <div
          class="text-grey"
        >In our shop you can find many unique recipes that were carefully polished during almost 20 years of experie...</div>
        <div class="q-my-md" style="margin-left: -20px" :class="btnModify? 'btn-style': ''">
          <q-btn
            flat
            class="cart-btn"
            @mouseenter="btnModify = true"
            @mouseleave="btnModify = false"
          >
            <q-icon name="mdi-cart" class="cart-icon" :class="btnModify? 'bg-transparent': ''"></q-icon>
            <div class="q-ml-md q-mr-xs">Add to cart</div>
          </q-btn>
        </div>
      </q-card-section>
    </q-card>
  </div>
</template>
<script>
export default {
  data() {
    return {
      showImage: true,
      btnModify: false
    };
  }
};
</script>
<style lang="scss" scoped>
.shopping-card {
  width: 300px;
//    border-radius: 50px 50px 0px 0px;
  .cart-image {
    background-color: #f8f8f8;
    border-radius: 50px;
    padding: 20px;
  }
}
.cart-icon {
  background-color: #96ca2d;
  height: 60px;
  width: 60px;
  border-radius: 48%;
  color: white;
}

.btn-style {
  margin-left: -20px;
  border: 2px solid gray;
  border-radius: 70px;
  width: 77.7%;
  padding: 2px;

  transition: 0.5s ease-in-out;
  .cart-btn {
    background-color: grey;
    border-radius: 50px;
    color: white;
    transform: scale(0.96);
  }
}
</style>
