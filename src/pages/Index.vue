<template>
  <q-page class="q-ma-xl">
    <div class="row justify-center">
      <div class="col-sm-4 col-xs-12 q-my-lg">
        <discount-card></discount-card>
      </div>
      <div class="col-sm-4 col-xs-12 q-my-lg">
        <coffee-cart-card></coffee-cart-card>
      </div>
      <div class="col-sm-4 col-xs-12 q-my-lg">
        <shopping-cart></shopping-cart>
      </div>
    </div>
  </q-page>
</template>

<script>
import DiscountCard from "../components/DiscountCard";
import CoffeeCartCard from "../components/CoffeeCartCard";
import ShoppingCart from "../components/ShoppingCart";
export default {
  name: "PageIndex",
  components: { DiscountCard, CoffeeCartCard, ShoppingCart }
};
</script>
