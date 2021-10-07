
<template>
  <form action="/charge" method="post" id="payment-form">
    <div class="form-row">
      <label for="card-element">
        クレジット・デビットカード番号
      </label>
      <div id="card-element">
        <!-- Stripe Element がここに入ります。 -->
      </div>

      <!-- Element のエラーを入れます。 -->
      <div id="card-errors" role="alert"></div>
    </div>

    <button>お支払い</button>
  </form>
</template>

<script>

export default {
  mounted() {
    this.stripeDemo()
  },
  methods: {
    stripeDemo() {
      var elements = this.$stripe.elements();
      console.log(elements);
      // card Element のインスタンスを作成
      var card = elements.create('card');
  
      // マウント
      card.mount('#card-element');
    }
  },
}

</script>

<style>

</style>

