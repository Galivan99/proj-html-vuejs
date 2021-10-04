<template>
  <div class="col-3 secondary-post p-4 mx-4 h-350 white">
    <div class="post-details my-5">
      <time>{{ info.time }}</time>
      <span> &bull; <span>By Paul</span></span>
    </div>
    <h5 class="my-5">
      {{ info.title }}
    </h5>
    <p class="my-5">
      {{ info.text }}
    </p>
    <button type="button" class="btn white-back black-text mt-5">
      Read More
    </button>
  </div>
</template>

<script>
export default {
  name: "CardArticle",
  props: ["info"],
};
</script>

<style scoped lang="scss">
@import "../assets/scss/var.scss";
@import "../assets/scss/_generics.scss";
.secondary-post {
  border-radius: 20px;
  background-color: $section-background;
}
button {
  background-color: #fff;
  border-radius: 10px;
  &.black-text {
    color: #000;
  }
  &:hover {
    border: 2px solid $section-background;
  }
}
</style>