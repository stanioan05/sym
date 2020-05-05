<template>
  <div class="main_container" id="hero">
    <div class="navbar">
      <div class="search-screen">
        <i class="fas fa-search search-icon"></i>
        <div class="search-box">
          <input type="text" class="search-txt" placeholder="type here to search" />
          <button class="search-btn">
            <i class="fas fa-arrow-right"></i>
          </button>
        </div>
      </div>
      <div class="navbar_items">
        <ul>
          <li>
            <router-link to="/">
              <a class="nav">Home</a>
            </router-link>
          </li>
          <li>
            <router-link to="/about">
              <a class="nav">About</a>
            </router-link>
          </li>
          <li>
            <router-link to="/about">
              <a class="nav">About</a>
            </router-link>
          </li>
        </ul>
      </div>
    </div>
    <div class="banner_image">
      <img class="sol" src="logo.svg" />
    </div>
    <p class="logo">Symphonia Software</p>
    <div>
      <router-view></router-view>
    </div>
    <div>
      <footer>
        <div class="footer-container">
          <div class="left-col">
            <div class="back-to-top tooltip">
              <span class="tooltiptext">Back to top</span>
              <a href="#hero">
                <i class="fas fa-chevron-up"></i>
              </a>
            </div>
            <div class="banner_image">
              <img class="sol" src="logo.svg" />
            </div>
            <p class="logo">Symphonia Software</p>
            <div class="social-media">
              <a href="#">
                <i class="fab fa-facebook-f"></i>
              </a>
              <a href="#">
                <i class="fab fa-twitter"></i>
              </a>
              <a href="#">
                <i class="fab fa-instagram"></i>
              </a>
              <a href="#">
                <i class="fab fa-youtube"></i>
              </a>
              <a href="#">
                <i class="fab fa-linkedin-in"></i>
              </a>
            </div>
            <p class="rights-text">© 2020 Created By Symphonia Software All rights Reseved.</p>
          </div>
        </div>
      </footer>
    </div>
  </div>
</template>

<script>
import About from "./views/About.vue";
import Home from "./views/Home.vue";
import Contact from "./views/Contact.vue";
export default {
  components: {
    About,
    Home,
    Contact
  }
};
</script>




<style>
:root {
  --first-color: #047a93;
  --second-color: #d3def0;
  --bcg-color: #24222b;
  --radiant: linear-gradient(
    90deg,
    rgb(36, 34, 71) 0%,
    rgb(38, 38, 65) 0%,
    rgba(4, 122, 147, 1) 100%
  );
}

html {
  scroll-behavior: smooth;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  outline: none;
  list-style: none;
  text-decoration: none;
  font-family: "Work Sans", sans-serif;
}

body {
  background: var(--bcg-color);
}
.main_container {
  position: relative;
}
.back-to-top {
  position: absolute;
  background-color: var(--bcg-color);
  right: 20px;
  top: 270px;
  transform: translateX(-50%);
  float: right;
}

.back-to-top i {
  display: block;
  color: var(--first-color);
  padding: 1em;
  background: var(--bcg-color);
  border-radius: 50%;
  font-size: 16px;
}

.back-to-top i:hover {
  background: var(--second-color);
  color: var(--bcg-color);
  box-shadow: 0 0 5px var(--first-color), 0 0 15px var(--first-color);
}
/* tooltip */

.tooltip {
  position: relative;
  display: inline-block;
}

.tooltip .tooltiptext {
  visibility: hidden;
  position: absolute;
  width: 150px;
  background-color: var(--bcg-color);
  color: var(--second-color);
  text-align: center;
  padding: 5px;
  margin-bottom: 10px;
  left: 50%;
  bottom: 100%;
  font-size: 12px;
  margin-left: -75px;
  letter-spacing: 2px;
  font-weight: 600;
  opacity: 0;
  transition: opacity 2s;
  text-transform: uppercase;
}

::selection {
  background: #a200ff;
}

.tooltip:hover .tooltiptext {
  visibility: visible;
  opacity: 1;
}

.about {
  display: grid;
  grid-template-columns: repeat(6, 1fr);
  grid-gap: 30px;
}

.story {
  color: var(--second-color);
  text-align: center;
  word-spacing: 2px;
  line-height: 1.4;
  font-size: 1.1em;
  grid-area: 2 / 2 / 4 / 6;
  text-indent: 30px;
  /* max-width: 100ch; */
}
.story::first-letter {
  font-size: 2em;
  color: var(--first-color);
  font-weight: 700;
}
.story-1 {
  color: var(--second-color);
  text-align: center;
  word-spacing: 2px;
  line-height: 1.4;
  font-size: 1.1em;
  grid-area: 4 / 2 / 7 / 6;
  text-indent: 30px;
  /* max-width: 100ch; */
}

.story-1::first-letter {
  font-size: 2em;
  color: var(--first-color);
  font-weight: 700;
}

.story-2 {
  color: var(--second-color);
  text-align: center;
  word-spacing: 2px;
  line-height: 1.4;
  font-size: 1.1em;
  grid-area: 7 / 2 / 10 / 6;
  text-indent: 30px;
  /* max-width: 100ch; */
}
.story-2::first-letter {
  font-size: 2em;
  color: var(--first-color);
  font-weight: 700;
}

h1.title {
  margin-bottom: 20px;
  margin-right: 25px;
  color: var(--second-color);
  font-size: 2.6em;
  word-spacing: 25px;
  letter-spacing: 5px;
  text-align: center;
  justify-content: space-between;
  align-items: center;
}

/* buttons */

.btn a {
  display: block;
  width: 180px;
  height: 35px;
  border: 1px solid var(--first-color);
  border-radius: 25px;
  line-height: 35px;
  margin: 25px auto;
  color: var(--second-color);
  text-align: center;
  text-transform: uppercase;
  font-size: 1em;
}

.button {
  background: none;
  border: 1px solid var(--first-color);
  color: var(--second-color);
  padding: 6px 12px;
  border-radius: 25px;
  text-transform: uppercase;
  display: inline-block;
  font-size: 1em;
  cursor: pointer;
}

.button:hover,
.btn a:hover {
  box-shadow: 0 0 5px var(--first-color), 0 0 15px var(--first-color);
  transition: 0.3s all;
  transform: scale(1.02);
}

/* navbar */

.navbar {
  width: 100%;
  height: 65px;
  display: flex;
  justify-content: space-around;
  align-items: center;
  text-align: center;
  position: sticky;
  top: 0;
  background: var(--radiant);
}

a.nav {
  border-radius: 25px;
  font-size: 1em;
  margin: 10px;
  padding: 5px 15px 5px 15px;
}
a.home {
  border-radius: 25px;
  font-size: 1em;
  /* margin: 5px; */
  padding: 5px 35px 5px 35px;
}

a.nav:hover,
a.home:hover {
  box-shadow: 0 0 5px var(--second-color), 0 0 15px var(--second-color);
  transition: 0.3s all;
  opacity: 0.7;
}

.navbar .navbar_items ul {
  display: flex;
}

.navbar .navbar_items ul li {
  text-transform: uppercase;
}

.navbar .navbar_items ul li a {
  color: var(--second-color);
  font-weight: 700;
  letter-spacing: 2px;
  color: wheat;
}
/*  */

.banner_image {
  display: flex;
  justify-content: center;
  align-items: center;
}

section img {
  width: 200px;
  height: 200px;
  border-radius: 10px;
  /* opacity: 0.5; */
}

/* section img:hover {
  transform: scaleX(-1);
} */

h4 {
  color: var(--second-color);
  font-size: 1.5em;
}

#skills {
  padding: 30px;
  text-align: center;
}

#skills ul {
  margin: 40px 0;
}
#skills li {
  padding: 10px;
  grid-column: span 4;
  text-align: center;
}

#skills img {
  margin: 10px auto;
}

.grid {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  gap: 50px;
  box-sizing: border-box;
}

#portfolio {
  padding: 30px;
  text-align: center;
}
#portfolio ul {
  margin: 40px 0;
}

#portfolio li {
  grid-column: span 4;
  text-align: center;
  padding: 10px;
}
#portfolio img {
  margin: 10px auto;
}
#skills li:nth-child(2),
#portfolio li:nth-child(2) {
  margin-top: 50px;
}

/* footer */

footer {
  height: auto;
  background: var(--radiant);
  padding: 30px;
}

.footer-container {
  padding: 0 20px;
  justify-content: space-between;
  align-items: center;
  background: var(--bcg-color);
}

.social-media {
  margin: 10px;
}

.social-media a {
  color: var(--second-color);
  font-size: 22px;
  text-decoration: none;
  transition: 0.3s linear;
  align-items: center;
  justify-content: space-between;
  text-align: center;
  padding: 10px;
}

.social-media a:hover {
  color: var(--first-color);
}

.rights-text {
  color: var(--second-color);
  font-size: 1.1em;
  line-height: 20px;
  padding: 20px;
  text-align: center;
}

.logo {
  color: var(--second-color);
  font-size: 1.8em;
  text-align: center;
  word-spacing: 25px;
  letter-spacing: 5px;
  text-transform: uppercase;
  margin-bottom: 30px;
  font-family: "Monoton", cursive;
  align-items: center;
}

/* contact */

#contact {
  padding: 30px 20px;
}

#contact h3,
#contact p {
  margin-bottom: 0;
  text-align: center;
}
#contact form {
  width: 80%;
  max-width: 400px;
  margin: 20px auto;
  text-align: center;
}

#contact textarea,
#contact input {
  width: 100%;
  margin: 10px 0;
}
#contact textarea {
  overflow: hidden;
  max-width: 100%;
  height: 100px;
}

#contact .button {
  margin-top: 10px;
}

.name:hover,
.email:hover,
.tele:hover,
.place:hover {
  transform: scale(1.02);
}

/* .name,
.tele {
  border-top-left-radius: 25px;
  border-top-right-radius: 25px;
  text-transform: uppercase;
}
.email,
.place {
  border-bottom-left-radius: 25px;
  border-bottom-right-radius: 25px;
} */

input,
textarea {
  padding: 10px 16px;
  border: 1px solid var(--first-color);
  color: rgb(255, 255, 255);
  outline: none;
  font-size: 1em;
  caret-color: var(--first-color);
  background-image: var(--radiant);
  letter-spacing: 2px;
  border-radius: 25px;
  text-transform: uppercase;
}

::placeholder {
  color: wheat;
  /* font-weight: 700; */
}

.contact-info {
  display: flex;
  margin: auto;
  width: 100%;
  align-items: center;
  justify-content: space-between;
  padding: 0 20px;
}

.card {
  width: calc(33% - 20px);
  height: 100px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  color: var(--second-color);
  cursor: pointer;
  margin-top: 30px;
}

.card-icon {
  font-size: 28px;
  background: var(--first-color);
  width: 60px;
  height: 60px;
  text-align: center;
  line-height: 60px !important;
  border-radius: 50%;
  transition: 0.3s linear;
}

.card:hover .card-icon {
  background: none;
  color: var(--first-color);
  border: 1px solid var(--first-color);
}

.card p {
  margin-top: 30px;
  letter-spacing: 2px;
  transition: 0.3s linear;
  color: var(--second-color);
  font-size: 1.1em;
}

/* search */

.search-screen,
.search-icon {
  position: absolute;
  top: 0;
  right: 0;
  width: 50px;
  height: 65px;
}

.search-icon {
  text-align: center;
  line-height: 60px !important;
  cursor: pointer;
  font-size: 18px;
  color: wheat;
}

.search-icon:hover {
  color: var(--second-color);
}

.search-box {
  width: 0;
  height: 0;
  position: absolute;
  overflow: hidden;
  opacity: 0;
  transition: opacity 0.3s linear;
  transition-delay: 0.5s;
}

.search-screen.active {
  position: fixed;
  background-image: var(--radiant);
  width: 100%;
  height: 100%;
}

.search-screen.active .search-box {
  opacity: 1;
  width: 360px;
  height: 50px;
  border: 1px solid var(--second-color);
  border-radius: 25px;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
}

.search-txt {
  border: 0;
  width: 100%;
  height: 100%;
  background: none;
  padding: 0 30px;
  color: var(--second-color);
  outline: none;
  margin-right: 50px;
}

.search-txt::placeholder {
  color: wheat;
  font-weight: 700;
  letter-spacing: 2px;
}

.search-btn {
  position: absolute;
  top: 0;
  right: 0;
  width: 50px;
  height: 100%;
  background: none;
  border: 0;
  outline: none;
  color: var(--second-color);
  cursor: pointer;
  font-size: 1.1em;
  transform: rotate(45deg);
  opacity: 0;
  transition: 0.3s linear;
}

@media only screen and (min-width: 320px) and (max-width: 576px) {
  h1.title {
    text-align: center;
    font-size: 2em;
  }
  p.para {
    text-align: center;
    display: block;
    padding: 20px;
  }
  .contact-info {
    flex-direction: column;
  }

  .card {
    width: 100%;
    max-width: 300px;
    margin: 10px 0;
  }

  .grid {
    grid-template-columns: 1fr;
  }
  section img {
    width: 120px;
    height: 120px;
  }
  h4 {
    font-size: 1em;
  }
  .sol {
    width: 120px;
    height: 120px;
  }
}

@media only screen and (min-width: 576px) and (max-width: 768px) {
  h1.title {
    text-align: center;
    font-size: 2.2em;
  }
  p.para {
    text-align: center;
    display: block;
    padding: 20px;
  }
  .contact-info {
    flex-direction: column;
  }

  .card {
    width: 100%;
    max-width: 300px;
    margin: 10px 0;
  }

  .grid {
    grid-template-columns: 1fr;
  }
  section img {
    width: 140px;
    height: 140px;
  }
  h4 {
    font-size: 1.2em;
  }
  .sol {
    width: 140px;
    height: 140px;
  }
}

@media only screen and (min-width: 768px) and (max-width: 992px) {
  h1.title {
    text-align: center;
    font-size: 2.4em;
  }
  p.para {
    text-align: center;
    display: block;
    padding: 20px;
  }
  .contact-info {
    flex-direction: column;
  }

  .card {
    width: 100%;
    max-width: 300px;
    margin: 10px 0;
  }

  .grid {
    grid-template-columns: 1fr;
  }
  section img {
    width: 180px;
    height: 180px;
  }
  h4 {
    font-size: 1.4em;
  }
  .sol {
    width: 180px;
    height: 180px;
  }
}
</style>
