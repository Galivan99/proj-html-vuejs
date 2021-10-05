<template>
  <div class="row justify-content-center card-price">
    <div
      class="col-3 position-relative"
      v-for="info in pricingInfos"
      :key="info.price"
    >
      <div class="card text-center p-5" :class="info.backgroundClass">
        <p class="price-background">{{ info.price }}</p>
        <h3>
          <strong>{{ info.service }}</strong>
        </h3>
        <p>{{ info.forWho }}</p>
        <p>$</p>
        <p class="h1">{{ info.price }}</p>
        <p>Per Month</p>
        <p>{{ info.detailOne }}</p>
        <p>{{ info.detailTwo }}</p>
        <p>{{ info.detailThree }}</p>
        <p>{{ info.detailFour }}</p>
        <p>{{ info.detailFive }}</p>
        <div class="btn-container d-flex justify-content-center mt-4">
          <button type="button" class="btn" :class="info.backgroundButton">
            Order Now <i class="fas fa-long-arrow-alt-right ms-3"></i>
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardPrice",
  props: ["pricingInfos"],
};
</script>

<style scoped lang="scss">
.card {
  display: flex;

  border-radius: 20px;
  border-color: transparent;
  box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
}
button {
  width: 140px;
  border-radius: 25px;
  color: #fff;
}
.pink-button {
  background: rgb(191, 44, 110);
  background: linear-gradient(
    180deg,
    rgba(191, 44, 110, 1) 0%,
    rgba(244, 90, 103, 1) 95%
  );
  border-color: transparent;
}
.pink-card {
  background: rgb(191, 44, 110);
  background: linear-gradient(
    170deg,
    rgba(191, 44, 110, 1) 0%,
    rgba(244, 90, 103, 1) 95%
  );
  color: #fff;
}
.price-background {
  position: absolute;
  top: -78px;
  left: 117px;
  color: rgba(0, 0, 0, 0.08);
  font-size: 200px;
  font-weight: bold;
}
</style>