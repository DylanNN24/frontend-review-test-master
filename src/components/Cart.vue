<template>
  <div class="cart-list">
    <div v-for="item in spisok_dlya_rendera">
    <span> {{ item.title }} - </span>
    <span>   {{ item.price }} * </span>
    <span>   {{ item.amount }} = </span>
    <span>   {{ Math.round(item.amount * item.price * 100) / 100  }} {{ currency }} </span>
     
    
    </div>

  </div>
</template>

<script>
export default {
  props: {
    cart: Array,
    currency: String,
  },
  computed: {
      spisok_dlya_rendera() {
          return this.cart.reverse();
      },
  },
};
</script>

<style>

</style>
