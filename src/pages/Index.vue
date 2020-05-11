<template>
  <q-page class="q-ma-xl">
    <div class="row justify-center">
      <div class="col-sm-4 col-xs-12">
        <discount-card></discount-card>
      </div>
      <div class="col-sm-4 col-xs-12">
        <coffee-cart-card></coffee-cart-card>
      </div>
    </div>
  </q-page>
</template>

<script>
import DiscountCard from "../components/DiscountCard";
import CoffeeCartCard from "../components/CoffeeCartCard";
export default {
  name: "PageIndex",
  components: { DiscountCard, CoffeeCartCard }
};
</script>
