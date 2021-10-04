<template>
  <main>
    <!-- SEZIONE WHAT WE DO -->
    <section id="what-we-do">
      <div class="container">
        <!-- Row for Title -->
        <div class="row py-5">
          <div class="col-12 text-center">
            <p class="pink-p">Our Services</p>
            <h3 class="fs-25p"><strong>What</strong> We Do</h3>
            <p class="py-2">
              When, while the lovely valley teems with vapour around meand the
              meridian sun strikes the upper surface .
            </p>
          </div>
        </div>
        <!-- Row for Services -->
        <div class="row align-items-center">
          <div
            v-for="(service, index) in services"
            :key="index"
            class="col-3 p-50 text-center"
          >
            <Services :service="service"></Services>
          </div>
        </div>
        <!-- Row for Button -->
        <div class="row py-5">
          <div class="col-12 text-center">
            <button
              class="mx-3 gradient-pink btn button-box-shadow"
              type="button"
            >
              View All Services
            </button>
          </div>
        </div>
      </div>
    </section>
    <!-- SEZIONE START YOUR PROJECT -->
    <section id="start-your-project">
      <div class="container h-100">
        <div class="row h-100 align-items-center">
          <div class="col-6 pt-10 px-5">
            <div class="start-project-img-container">
              <img
                class="img-fluid background-men"
                src="@/assets/img/nemoodar.png"
                alt="start-project-img"
              />
              <img
                class="img-fluid men-data"
                src="@/assets/img/men-data.png"
                alt="start-project-img"
              />
            </div>
          </div>
          <div class="col-6 basis-40 white">
            <p class="py-2">Start Your Project</p>
            <h1 class="py-3">
              <strong>Grow Your Business</strong>
              With Our Strategy
            </h1>
            <p class="py-3 azul-color">
              When, while the lovely valley teems with vapour around meand the
              meridian sun strikes the upper surface. of the impentrable follage
              of my trees, and but a few stray gleams steal into the inner
              sanctuary
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
        </div>
      </div>
    </section>
    <!-- SEZIONE LATEST WORK -->
    <section id="latest-work">
      <div class="container">
        <!-- Row for title -->
        <div class="row justify-content-between">
          <div class="col-4 section-title mt-4">
            <p class="light-grey">Portfolio</p>
            <h3 class="fs-25p"><strong>latest</strong> work</h3>
          </div>
          <div
            class="
              col-4
              arrow-buttons
              d-flex
              mt-4
              align-items-center
              justify-content-end
            "
          >
            <!-- Utilizzate queste frecce perchè quelle della traccia erano a pagamento su Font Awesome -->
            <i class="fs-3 fas fa-arrow-circle-left me-3 clickable"></i>
            <i class="fs-3 fas fa-arrow-circle-right clickable"></i>
          </div>
        </div>
      </div>
      <!-- Row for Slider -->
      <div class="row justify-content-center m-3">
        <div
          v-for="(workDetail, index) in workDetails"
          :key="index"
          class="col-4 clickable"
        >
          <Work :workDetail="workDetail"></Work>
        </div>
      </div>
      <!-- Row for dots controllers -->
      <div class="row justify-content-center my-4">
        <div class="col d-flex justify-content-center">
          <div class="dot dot-active clickable"></div>
          <div class="dot clickable"></div>
          <div class="dot clickable"></div>
          <div class="dot clickable"></div>
          <div class="dot clickable"></div>
        </div>
      </div>
    </section>
    <!-- SEZIONE OUR PRICING -->
    <section id="our-pricing" class="pt-4">
      <div class="container-fluid">
        <!-- Row for title -->
        <div class="row title-price">
          <div class="col text-center mb-5">
            <p class="pink-p"><strong>Price List</strong></p>
            <h4 class="fs-2 white"><strong>Our</strong> Pricing</h4>
            <p class="white">
              When, while the lovely valley teems with vapour around meand the
              meridian sun strikes the upper surface .
            </p>
          </div>
        </div>
        <!-- Row for price details -->
        <CardPrice :pricingInfos="pricingInfos"></CardPrice>
      </div>
    </section>
    <!-- SEZIONE LATEST POSTS -->
    <section id="latest-posts">
      <div class="container">
        <!-- Row For Title Section -->
        <div class="row text-center mb-5">
          <p class="pink-p">Blog</p>
          <h3 class="fs-25p"><strong>Latest</strong> Posts</h3>
          <p>
            When, while the lovely valley teems with vapour around meand the
            meridian sun strikes the upper surface .
          </p>
        </div>
        <div class="row">
          <!-- Row per i posts -->
          <div class="col-5 white main-post h-350">
            <div class="layover d-flex align-items-end p-5">
              <div class="article-preview">
                <div class="post-details my-2 ">
                  <time>April 21, 2019</time>
                  <span> &bull; <span>By Paul</span></span>
                </div>
                <h5 class="my-2">
                  Amazon gets CCI not to acquire 49% stake in
                </h5>
                <p class="my-2">
                  When, while the lovely valley teems with vapor around me, and
                  the meridiana sun s...
                </p>
              </div>
              <button type="button" class="btn white-back mt-5 w-100p">
                Read More
              </button>
            </div>
          </div>

          <CardArticle
            v-for="(info, index) in articlesInfos"
            :key="index"
            :info="info"
          ></CardArticle>
        </div>
      </div>
    </section>
    <!-- SEZIONE WHAT PEOPLE SAY -->
    <section id="people-say">
      <div class="container">
        <!-- Row for Title -->
        <div class="row">
          <div class="col my-5 text-center">
            <p class="pink-p">Testimonial</p>
            <h3 class="fs-25p"><strong>What</strong> People Say</h3>
            <p>
              When, while the lovely valley teems with vapour around meand the
              meridian sun strikes the upper surface .
            </p>
          </div>
        </div>
        <!-- Row per le immagini e recensioni delle persone -->

        <div class="row justify-content-center">
          <div
            class="
              col-3
              d-flex
              flex-column
              align-items-center
              position-relative
              px-5
            "
          >
            <div
              class="first people-img-container d-flex justify-content-center"
            >
              <img
                class="img-fluid"
                src="../assets/img/szabo-viktor-1266895-unsplash-1024x1024.png"
                alt="First Person"
                First
                People
              />
            </div>
            
            <div class="stars my-5">
              <i class="fas fa-star"></i>
              <i class="fas fa-star"></i>
              <i class="fas fa-star"></i>
              <i class="far fa-star"></i>
              <i class="far fa-star"></i>
            </div>
            <div class="caption text-center">
              <p class="my-5">
                When, while lovely valley teems with vapour around meand
                meridian sun strikes the upper impenetrable follage of my trees,
                and but a thousand.
              </p>
              <span class="fw-bold my-3">Michkel Anegl</span>
              <p>Marketing Management</p>
            </div>
          </div>
          <div
            class="
              col-3
              d-flex
              flex-column
              align-items-center
              position-relative
              mx-3
            "
          >
            <div class="second people-img-container">
              <img
                class="img-fluid"
                src="../assets/img/philipe-cavalcante-539505-unsplash-1024x1024.png"
                alt="Second Person"
              />
            </div>
            

            <div class="stars my-5">
              <i class="fas fa-star"></i>
              <i class="fas fa-star"></i>
              <i class="fas fa-star"></i>
              <i class="far fa-star"></i>
              <i class="far fa-star"></i>
            </div>
            <div class="caption text-center">
              <p class="my-5">
                When, while lovely valley teems with vapour around meand
                meridian sun strikes the upper impenetrable follage of my trees,
                and but a thousand.
              </p>
              <span class="fw-bold my-3">Michkel Anegl</span>
              <p>Marketing Management</p>
            </div>
          </div>
          <div
            class="
              col-3
              d-flex
              flex-column
              align-items-center
              position-relative
            "
          >
            <div class="third people-img-container">
              <img
                class="img-fluid"
                src="../assets/img/fabio-spinelli-695744-unsplash-1024x1024.png"
                alt="Third Person"
              />
            </div>
            

            <div class="stars my-5">
              <i class="fas fa-star"></i>
              <i class="fas fa-star"></i>
              <i class="fas fa-star"></i>
              <i class="far fa-star"></i>
              <i class="far fa-star"></i>
            </div>
            <div class="caption text-center">
              <p class="my-5">
                When, while lovely valley teems with vapour around meand
                meridian sun strikes the upper impenetrable follage of my trees,
                and but a thousand.
              </p>
              <span class="fw-bold my-3">Michkel Anegl</span>
              <p>Marketing Management</p>
            </div>
          </div>
        </div>
        <!-- Row per i clienti -->
        <div id="customers" class="row">
          <div class="col">
            <img src="../assets/img/client-1-1.png" alt="Golden Golden" />
          </div>
          <div class="col">
            <img src="../assets/img/clienty-2.png" alt="Sweety Cafeteria" />
          </div>
          <div class="col">
            <img src="../assets/img/clienty-4.png" alt="Fastlane" />
          </div>
          <div class="col">
            <img src="../assets/img/client-5.png" alt="Mighty Furniture" />
          </div>
          <div class="col">
            <img src="../assets/img/clienty-3.png" alt="Jack Roller" />
          </div>
        </div>
      </div>
    </section>
    <section id="subscription">
      <div class="container">
        <div
          class="
            row
            align-items-center
            justify-content-between
            subscription-box
            gradient-pink
            p-4
          "
        >
          <div class="col-6">
            <h3 class="fw-bolder fs-2 white">We Offer Awesome Services</h3>
            <p class="white">
              When, while lovely valley teems with vapour around meand meridian
              sun strikes the upper surface .
            </p>
          </div>
          <div class="col-6">
            <div class="input-subscription d-flex justify-content-between">
              <input type="text" placeholder="Enter Your Email Address" />
              <button type="button" class="btn gradient-blue">Subscribe</button>
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
import CardPrice from "@/components/CardPrice.vue";
import CardArticle from "@/components/CardArticle.vue";
import Services from "@/components/Services.vue";
import Work from "@/components/Work.vue";
export default {
  name: "Main",
  components: { CardPrice, CardArticle, Services, Work },
  props: ["pricingInfos", "articlesInfos", "services", "workDetails"],
};
</script>
<style scoped lang="scss">
@import "../assets/scss/_generics.scss";
@import "../assets/scss/var.scss";
//   Sezione Start your Project
#start-your-project {
  height: 520px;
  background-color: $section-background;
}
.background-men {
  position: absolute;
  top: -200px;
  left: 140px;
}
.men-data {
  position: absolute;
  top: -160px;
  left: 140px;
}
#start-your-project .start-project-img-container {
  width: 50%;
  position: relative;
}
// Sezione Latest Work
#latest-work {
  height: 750px;
}
.dot {
  width: 8px;
  height: 8px;
  margin: 4px;
  background-color: #e5e5ea;
  border-radius: 50%;
}
.dot-active {
  background-color: #db476c;
}
// Sezione Our Pricing
#our-pricing {
  background-color: $section-background;
  height: 300px;
}
.pink-p {
  color: #F9636B;
}
//  Sezione Latest Posts
#latest-posts {
  margin-top: 350px;
  button {
    background-color: #fff;
    border-radius: 10px;
    color: #000;
  }
}
.main-post {
  background-image: url("../assets/img/headway-537308-unsplash-1380x703.jpg");
  background-position: center;
  background-size: cover;
  border-radius: 20px;
}
// Sezione What People Say
.people-img-container {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  border: 4px solid #b6256f;
  background-size: contain;
  display: flex;
  justify-content: center;
}
.stars {
  color: #F9636B;
}
#customers {
  margin: 150px 0;
  .col {
    flex-basis: calc(100% / 5);
  }
}
// Sezione Subscription
.subscription-box {
  height: 150px;
  border-radius: 20px;
}
.input-subscription {
  background-color: #fff;
  border-radius: 20px;
  width: 50%;
  height: 35px;
  padding: 5px;
  input {
    border-color: transparent;
  }
  button {
    border-radius: 20px;
  }
}
</style>