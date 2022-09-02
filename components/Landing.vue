<template>
  <div>
    <div class="image-container grid-container">
      <div class="info-container grid-container">
        <div class="logo-container">
          <img :src="foundersPlaceLogo" />
        </div>
        <div class="title-container">
          <h4>A place where innovation <br />meets inspriation</h4>
        </div>
        <div class="hook-container">
          <h4 style="padding-bottom: 3em;">COMING SOON</h4>
          <h4 style="color: #9b493c">FOR UPDATES SIGN UP BELOW</h4>
        </div>
      </div>
    </div>
    <div class="grid-container-2">
      <div class="paragraph-container">
        <div class="content-container">
          <div class="container">
            <h1>
              Lorem ipsum dolar<br />
              est casta
            </h1>
            <p>
              Set in the heart of the establishedd Stephenson Quarter, adjacent
              to Newcastle upon Tyne's central railway station, with commanding
              views over the River Tyne - Founders Place is a new district of
              the city brining purpose to its surroundings. It's reimagined,
              redesigned and revitalised in a spirit true to the place's
              history.
            </p>
          </div>
        </div>
      </div>
      <div class="form-container">
        <div class="content-container">
          <div class="container">
            <h1>Sign up <br />for updates</h1>
            <form>
              <input
                class="personal-input"
                type="text"
                placeholder="Full Name"
              />
              <input class="personal-input" type="text" placeholder="Surname" />
              <input
                class="email-input"
                type="text"
                placeholder="Email Address"
              />
              <div class="checkbox-container">
                <input class="checkbox-input" type="checkbox" />
                <label class="form-disclaimer" for="checkbox">
                  I agree for HTA Real Estate to use the submitted information
                  for marketing and direct communications
                </label>
              </div>
              <input class="submit-button" type="submit" value="Submit" />
            </form>
            <div class="developments-div">
              <h3>Our on site developments</h3>
              <img class="developments-logo-pattern" :src="images[2]" />
              <img class="developments-logo-pioneer" :src="images[1]" />
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="footer-container">
      <div class="social-logos-mobile">
        <img
          class="social-icon"
          :src="socials[3]" />
        <img
          class="social-icon"
          :src="socials[2]" />
        <img
          class="social-icon"
          :src="socials[1]" />
        <img
          class="social-icon"
          :src="socials[0]" />
      </div>
      <img class="founders-logo" :src="foundersPlaceLogo" />
      <div class="footer-content">
        <div class="social-logos">
          <img
            class="social-icon"
            :src="socials[3]" />
          <img
            class="social-icon"
            :src="socials[2]" />
          <img
            class="social-icon"
            :src="socials[1]" />
          <img
            class="social-icon"
            :src="socials[0]" />
        </div>
        <div class="footer-links">
          <p class="copyright">@The Pioneer</p>
          <p class="link">Site Map</p>
          <p class="tcs">Terms & Conditions</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// imports
import foundersPlaceLogo from '~/assets/LandingPages/Founders/founders-place-logo-01.svg'
import heroImage1 from '~/assets/LandingPages/Pioneer/hero-image-2.jpg'
import pioneerLogo1 from '@/assets/LandingPages/Pioneer/pioneer-logo-01.svg'
import patternLogo from '~/assets/LandingPages/Pattern/pattern-shop-logo-02-01.svg'
import facebookIcon from '~/assets/LandingPages/Socials/facebook-svg-g.svg'
import twitterIcon from '~/assets/LandingPages/Socials/twitter-svg-g.svg'
import youtubeIcon from '~/assets/LandingPages/Socials/youtube-svg-g.svg'
import instagramIcon from '~/assets/LandingPages/Socials/instagram-svg-g.svg'

export default {
  name: 'MainLanding',
  data() {
    return {
      images: [heroImage1, pioneerLogo1, patternLogo],
      foundersPlaceLogo,
      socials: [instagramIcon, twitterIcon, youtubeIcon, facebookIcon],
    }
  },
}
</script>

<style>
@font-face {
  font-family: 'Solano Gothic M';
  src: url('~/assets/fonts/Solano Gothic Pro MVB Medium.ttf') format('truetype');
}
@font-face {
  font-family: 'Solano Gothic B';
  src: url('~/assets/fonts/Solano Gothic Pro MVB Bold.ttf') format('truetype');
}
@font-face {
  font-family: 'Contralto Big R';
  src: url('~/assets/fonts/Contralto Big Regular.ttf') format('truetype');
}
@font-face {
  font-family: 'Jost 300 Light';
  src: url('~/assets/fonts/Jost-300-Light.ttf') format('truetype');
}

body {
  margin: 0;
}

.grid-container {
  display: grid;
  background-color: #1c113b;
}

.grid-container-2 {
  display: grid;
  grid-template-columns: 50% 50%;
  background-color: #5f275c;
  padding-bottom: 2em;
}

.image-container {
  width: 100%;
  height: 100%;
  min-height: 700px;
  background-size: cover;
  background-position-y: -230px;
}

.image-container img {
  width: 100%;
}

.info-container {
  background-color: #1c113b;
  width: 95%;
  margin: 2em;
  text-align: center;
  opacity: 0.95;
}

.logo-container {
  padding: 0 1em 1em;
}

.logo-container img {
  width: 25%;
  margin: 0 auto;
  padding: 1em 0 3em;
}

.title-container {
  font-size: 5em;
  color: white;
  padding: 0.8em 0 0;
  font-family: 'Solano Gothic M', sans-serif;
  font-weight: 100;
  text-transform: uppercase;
  line-height: 72px;
}

.hook-container {
  color: #819050;
  padding: 5em 0 1em;
  font-size: 1.5em;
  font-family: 'Jost 300 Light', sans-serif;
  letter-spacing: 3px;
}

.content-container {
  width: 80%;
  margin: 2em auto;
}

.paragraph-container {
  margin: 0;
  padding: 0 0 0 1.5em;
  float: left;
  font-family: 'Contralto Big R', sans-serif;
}

.paragraph-container :is(h1, h2, h3, h4, h5, h6) {
  font-size: 2.5em;
  color: #c9e95f;
  line-height: 40px;
  font-family: 'Solano Gothic M', sans-serif;
  font-weight: 100;
}

.paragraph-container p {
  margin: 1.5em 0 0;
  font-size: 1.6em;
  text-align: left;
  width: 78%;
  color: white;
  font-family: 'Solano Gothic M', sans-serif;
  font-weight: 100;
}

.container {
  margin: 2em 0 0 3em;
  float: left;
}

.form-container {
  width: 100%;
  padding: 0;
  margin: 0;
  float: left;
  font-family: 'Contralto Big R', sans-serif;
}

.form-container form {
  margin: 0.5em 0;
  width: 90%;
  padding: 0;
  font-family: 'Solano Gothic M', sans-serif;
  font-weight: 100;
  font-size: 1.5em;
  color: white;
}

.form-container :is(h1, h2, h3, h4, h5, h6) {
  padding: 0 0 0.5em;
  font-size: 2.5em;
  color: #c9e95f;
  line-height: 40px;
  font-family: 'Solano Gothic M', sans-serif;
  font-weight: 100;
}

.personal-input {
  width: 45%;
  margin: 1em 0.5em 1em 0;
  padding: 1em 0;
  border-bottom: 1px solid white;
  border-top: none;
  border-left: none;
  border-right: none;
  background-color: #5f275c;
  font-size: 0.8em;
}

.email-input {
  width: 95%;
  margin: 1em 0.5em 1em 0;
  padding: 1em 0;
  border-style: none;
  border-bottom: 1px solid white;
  border-top: none;
  border-left: none;
  border-right: none;
  background-color: #5f275c;
  font-size: 0.8em;
}

.checbox-container {
  width: 100%;
}

.checkbox-input {
  width: 35px;
  height: 35px;
  margin: 0.5em 0 0;
  border: 1px solid #84ab8f;
}

.form-disclaimer {
  float: right;
  width: 80%;
  font-size: 0.6em;
  text-align: justify;
  padding: 0.6em 1em 1em 0.5em;
}

.submit-button {
  padding: 0.5em 0.8em;
  width: 50%;
  background-color: #c9e95f;
  border: 1px solid black;
  margin: 2em 0 1em;
}

.developments-div {
  padding: 1em 0;
  font-family: 'Solano Gothic M', sans-serif;
  font-weight: 100;
}

.developments-logo-pattern {
  width: 25%;
  float: left;
  padding: 0.5em 1em 0.5em 0;
}

.developments-logo-pioneer {
  width: 25%;
  float: left;
  padding: 1.9em 1em 2em;
}

.footer-container {
  margin: 0;
  width: 100%;
  padding: 2em 0 0;
  background-color: #1c113b;
  float: left;
  font-family: 'Contralto Big R', sans-serif;
}

.pioneer-logo {
  width: 15%;
  padding: 2em 1em 1em 3em;
  float: left;
}

.founders-logo {
  width: 15%;
  padding: 2em 0 1.8em 3em;
}

.footer-content {
  float: right;
  width: 50%;
  padding: 0 1em 0 2.3em;
}

.social-logos {
  width: 95%;
  float: left;
  padding-top: 1.5em;
}

.social-logos-mobile {
  display: none;
}

.social-icon {
  float: right;
  width: 8%;
  padding: 0.5em;
}

.footer-links {
  width: 100%;
  float: left;
  color: white;
  font-size: 0.8em;
  padding: 1em 0;
  font-family: 'Jost 300 Light', sans-serif;
}

.copyright {
  width: 48%;
  float: left;
  text-align: right;
}

.link {
  width: 18%;
  float: left;
  text-align: right;
}

.tcs {
  width: 30%;
  float: right;
  text-align: center;
}

@media screen and (max-width: 400px) {
  .image-container {
    background-position-y: 0;
  }

  .info-container {
    margin: 1.5em 0.6em;
  }

  .logo-container img {
    width: 72%;
  }

  .title-container {
    font-size: 3.4em;
    padding: 1.8em 0.5em 0.8em;
    line-height: 50px;
  }

  .hook-container {
    padding: 4em 0 2em;
  }

  .grid-container-2 {
    display: inline-block;
  }

  .paragraph-container {
    padding: 0;
  }

  .content-container {
    width: 90%;
  }

  .container {
    margin: 0;
  }

  .container :is(h1, h2, h3, h4, h5, h6) {
    float: left;
    width: 100%;
    text-align: center;
    font-size: 2.5em;
  }

  .container p {
    float: left;
    width: 100%;
    text-align: center;
    font-size: 1.3em;
  }

  .form-container form {
    margin: 0;
    text-align: center;
  }

  .form-container :is(h1, h2, h3, h4, h5, h6) {
    padding: 0 0 1em;
  }

  .personal-input {
    width: 100%;
  }

  .email-input {
    width: 100%;
  }

  .form-disclaimer {
    margin: 0;
  }

  .pioneer-logo {
    width: 80%;
    padding: 0;
    padding: 1em 1em 1em 2.3em;
  }

  .founders-logo {
    width: 80%;
    padding: 0;
    padding: 3em 1em 1em 2.3em;
  }

  .footer-content {
    float: left;
    width: 80%;
    padding: 2em 1em 0 2.3em;
  }

  .social-logos {
    display: none;
  }

  .social-icon {
    width: 14%;
    padding: 2em 1em;
  }

  .social-logos-mobile {
    display: block;
    width: 75%;
    margin: 0 auto;
  }

  .footer-links {
    width: 100%;
    float: left;
    color: white;
    font-size: 0.8em;
  }

  .copyright {
    width: 29%;
    float: left;
    text-align: left;
  }

  .link {
    width: 30%;
    float: left;
    text-align: right;
  }

  .tcs {
    width: 36%;
    float: left;
    float: right;
    text-align: right;
  }
}
</style>
