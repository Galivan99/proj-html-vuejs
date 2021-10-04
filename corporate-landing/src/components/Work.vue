<template>
  <div class="sliders-elements-container h-100">
    <div class="img-slider">
      <img
        class="img-fluid"
        :src="workDetail.url"
        :alt="workDetail.titleWork"
      />
    </div>
    <figcaption class="d-flex justify-content-between align-items-center">
      <span class="caption fw-bold">{{ workDetail.titleWork }}</span>
      <span class="light-grey caption">{{ workDetail.serviceType }}</span>
    </figcaption>
  </div>
</template>

<script>
export default {
  name: "Work",
  props: ["workDetail"],
};
</script>

<style scoped lang="scss">
figcaption {
  height: 40px;
  padding: 0 15px;
  border-bottom-right-radius: 30px;
  border-bottom-left-radius: 30px;
  .caption {
    font-size: 10px;
  }
}
.sliders-elements-container {
  box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
  border-bottom-right-radius: 30px;
  border-bottom-left-radius: 30px;
  &:hover figcaption {
    background: rgb(191, 44, 110);
    background: linear-gradient(
      90deg,
      rgba(191, 44, 110, 1) 0%,
      rgba(244, 90, 103, 1) 95%
    );
  }
  &:hover .caption {
    font-size: 10px;
    color: #fff;
  }
}
</style>