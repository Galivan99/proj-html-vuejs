<template>
  <div class="card-container d-flex flex-column align-items-center">
    <div class="img-container pb-3">
      <img class="img-fluid" :src="service.url" :alt="service.name" />
    </div>
    <h4 class="py-3">{{ service.name }}</h4>
    <p>
      {{ service.text }}
    </p>
    <div class="arrow-button gradient-pink">
      <i class="fas fa-arrow-right"></i>
    </div>
  </div>
</template>

<script>
export default {
  name: "Services",
  props: ["service"],
};
</script>

<style scoped lang="scss">
.card-container:hover {
  background-color: #08134a;
  border-radius: 20px;
  color: white;
  padding: 10 25px;
  cursor: pointer;
  .img-container {
    background-color: #fff;
  }
  .arrow-button {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 30px;
    height: 30px;
    border-radius: 50%;
  }
}
.img-container {
  width: 150px;
  border-radius: 20px;
}
.arrow-button {
  display: none;
}
</style>