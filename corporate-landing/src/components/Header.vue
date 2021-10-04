<template>
  <header class="bg-gradient-blu white">
    <div class="container">
      <div class="header-top">
        <div class="row align-items-center">
          <div class="col-6">
            <div class="img-container">
              <img
                class="img-fluid"
                src="../assets/img/white-logo-2.png"
                alt="Logo"
              />
            </div>
          </div>
          <div class="col-6 d-flex align-items-center">
            <nav class="d-flex">
              <li v-for="(link, index) in links" :key="index">
                <a :href="link.url"> {{ link.name }}</a>
              </li>
            </nav>
            <button class="h-50 ms-5 gradient-blue btn" type="button">
              Sign In
            </button>
          </div>
        </div>
      </div>
      <div class="header-bottom">
        <div class="row align-items-center">
          <div class="col-6 pt-10 px-5">
            <h1 class="py-3">
              <strong>Business Planning</strong> Digital Technology
              <strong>Modern Solution !</strong>
            </h1>
            <p class="py-3 azul-color">
              When, while the lovely valley teems with vapour around meand the
              meridian sun strikes the upper surface .
            </p>
            <div class="jumbo-buttons py-3">
              <button class="mx-3 gradient-pink btn try" type="button">
                Try It Now
              </button>
              <button class="mx-3 gradient-blue btn explore" type="button">
                Explore More
              </button>
            </div>
          </div>
          <div class="col-6">
            <div class="jumbo-img">
              <img
                class="img-fluid"
                src="@/assets/img/header.png"
                alt="header-img"
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  props: ["links"],
};
</script>

<style scoped lang="scss">
header {
  height: 680px;
  background-color: #08134a;
  li {
    list-style-type: none;
    margin: 15px;
    a {
      text-decoration: none;
      color: #fff;
    }
  }
}
.img-container {
  width: 100px;
}
</style>