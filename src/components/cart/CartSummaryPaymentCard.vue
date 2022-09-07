<template>
    <div class="cart-item-cart">
        <h3>Cart Total:{{cart_total.toFixed(2)}}</h3>
        <button class="view-product-button">Pay by credit card</button>
    </div>
</template>

<script>
export default {
    props:['products'],
    computed:{
        cart_total(){
             return this.$store.getters.cartItems.reduce((a, b) => a + (b.price * b.quantity), 0)
        }
    }
}
</script>
