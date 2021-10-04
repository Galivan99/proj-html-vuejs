<template>
  <!-- Invece che utilizzare il colore richiesto in secondo luogo dal committente (#f4f4f4) utilizzato sfondo blu poichè non potevo cambiare il colore del logo -->
  <footer>
    <div class="container">
      <div class="row pt-150p top-footer">
        <div class="col-3 white">
          <div class="img-container mb-5">
            <img
              class="img-fluid"
              src="../assets/img/white-logo-2.png"
              alt="Logo"
            />
          </div>
          <p class="caption">
            When, while lovely valley teems vapour aroundmeand meridian sun
            strikes the upper impenetrable
          </p>
        </div>
        <div class="col-3">
          <ul class="quick-links white">
            <strong>Quick Links</strong>
            <li><a href="#">Services</a></li>
            <li><a href="#">Contact</a></li>
            <li><a href="#">Blog</a></li>
          </ul>
        </div>
        <div class="col-3">
          <ul class="white">
            <strong>Resources</strong>
            <li><a href="#"> Art Design</a></li>
            <li><a href="#"> Computer</a></li>
            <li><a href="#"> IT News</a></li>
            <li><a href="#"> Networking</a></li>
            <li><a href="#"> Web Security</a></li>
          </ul>
        </div>
        <div class="col-3">
          <ul class="white pb-5">
            <strong>Contact Us</strong>
            <li>
              <a class="pb-4" href="#"
                ><strong class="white">Address:</strong> Patricia C. Amedee 4401
                Waldeck Street Grapevine Nashville Tx 76051</a
              >
            </li>
            <li>
              <a href="#"
                ><strong class="white">Phone: </strong> *99 (0) 101 0000 888</a
              >
            </li>
            <li>
              <a href="#"
                ><strong class="white">Email: </strong> info@yourdomain.com</a
              >
            </li>
          </ul>
        </div>
      </div>
    </div>
    <hr />
    <div class="container">
      <div class="row align-items-center bottom-footer">
        <div class="col-2"><p>&copy; 2020 Phlox. All Rights Reserved.</p></div>
        <div class="col-8"></div>
        <div class="col-2">
          <div class="icons white d-flex justify-content-evenly">
            <i class="fab fa-instagram"></i>
            <i class="fab fa-linkedin-in"></i>
            <i class="fab fa-facebook-f"></i>
            <i class="fab fa-twitter"></i>
            <i class="fas fa-arrow-circle-up"></i>
          </div>
          <div class="comment d-flex justify-content-center align-items-center">
            <i class="far fa-comment white"></i>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  props: ["links"],
};
</script>

<style scoped lang="scss">
@import "../assets/scss/var.scss";
footer {
  background-color: #08134a;
  height: 500px;
  hr {
    color: $light-grey;
  }
}
.pt-150p {
  padding-top: 150px;
}
.img-container {
  width: 300px;
}
.quick-links {
  padding-top: 10px;
}
li {
  list-style-type: none;
  padding: 7px 0;
  a {
    color: $light-grey;
    text-decoration: none;
  }
}
.caption {
  color: $light-grey;
}
.bottom-footer {
  position: relative;
  p {
    color: $light-grey;
  }
  .fa-arrow-circle-up {
    position: absolute;
    top: 0;
    right: 10px;
  }
}
.comment {
  position: absolute;
  top: 0;
  right: -30px;
  width: 25px;
  height: 25px;
  border-radius: 50%;
  background-color: #527ceb;
}
</style>