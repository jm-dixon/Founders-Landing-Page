<template>
  <div class="Signup">
    <h1 class="Signup__heading">Sign up<br>for updates</h1>
    <div class="Signup__name-wrapper">
      <input v-model="firstName" type="text" placeholder="Full name">
      <input v-model="lastName" type="text" placeholder="Surname">
    </div>
    <input v-model="email" type="text" placeholder="Email address">
    <div class="Signup__terms-wrapper">
      <input id="terms-conditions" v-model="acceptedTermsConditions" type="checkbox">
      <label for="terms-conditions" class="Signup__terms-label">
        I agree for Founders Place to use the submitted information
        for marketing and direct communications.
      </label>
    </div>
    <button type="submit" class="Signup__submit-button">Submit</button>

    <div class="Signup__brochure-download">
      <h1 class="Signup__heading">Our on site developments</h1>

      <div class="Signup__developments">
        <nuxt-link to="/" class="Footer__pattern-shop-logo-wrapper">
          <img :src="patternShopLogo" class="Footer__pattern-shop-logo-img">
        </nuxt-link>
        <nuxt-link to="/" class="Footer__pattern-shop-logo-wrapper">
          <img :src="thePioneerLogo" class="Footer__the-pioneer-logo-img">
        </nuxt-link>
      </div>
    </div>
  </div>
</template>

<script>
import brochureIcon from 'assets/images/THE PATTERNSHOP-Icon-Brochure-RGB.svg';
import PatternShopHorizLogoUrl from '@/assets/images/pattern-shop-logo-02-01.svg';
import FoundersPlaceLogoUrl from '@/assets/images/founders-place-logo-01.svg';
import ThePioneerLogoUrl from '@/assets/images/pioneer-logo-01.svg';

export default {
  name: 'Signup',

  data() {
    return {
      patternShopLogo: PatternShopHorizLogoUrl,
      foundersPlaceLogo: FoundersPlaceLogoUrl,
      thePioneerLogo: ThePioneerLogoUrl,
      firstName: '',
      lastName: '',
      email: '',
      acceptedTermsConditions: false,
      icons: {
        brochureIconUrl: brochureIcon
      }
    };
  },
}
</script>

<style lang="postcss">
@import "~/assets/css/settings/media-queries.css";
@import "~/assets/css/mixins/utils.css";

.Signup {
  @mixin interpolate padding-top, 5, 10;
  @mixin interpolate padding-bottom, 5, 10;

  width: 100%;
  padding-left: 15%;
  padding-right: 15%;
  background-color: var(--color-primary);

  @media (--phone-md) {
    padding-left: 8%;
    padding-right: 8%;
  }
}

.Signup__heading {
  margin-bottom: var(--spacing-xl);
  color: var(--color-secondary);
}

.Signup__name-wrapper {
  display: flex;
  flex-direction: column;
  width: 100%;
  margin-bottom: 2rem;
  gap: 1rem;

  @media (--tablet) {
    flex-direction: row;
  }
}

.Signup__terms-wrapper {
  display: flex;
  align-items: center;
  margin-top: 2rem;
}

input[type=text] {
  @mixin interpolate height, 4, 5.5;

  width: 100%;
  font-size: 2.4rem;
  padding: 14px 0;
  border-bottom: 1px solid var(--color-white);
  color: var(--color-white);
}

input[type=text]::placeholder {
  font-family: var(--font-default);
  color: var(--color-white);
  font-size: 3rem;
}

input[type=checkbox] {
  width: 3.5rem;
  height: 3.5rem;
  /* stylelint-disable */
  aspect-ratio: 1;
  /* stylelint-enable */
  background-color: var(--color-white);
  cursor: pointer;
  padding: 10px;
  color: var(--color-primary);
  font-size: 3rem;
}

input[type=checkbox]:checked::after {
  content: '\00d7';
  position: relative;
  top: -13px;
  left: -2px;
}

.Signup__terms-label {
  @mixin interpolate font-size, 1.1, 1.3;

  line-height: 1.3;
  margin-left: 2rem;
  cursor: pointer;
  color: var(--color-secondary);
}

.Signup__submit-button {
  @mixin interpolate font-size, 2, 2.6;
  @mixin interpolate padding-left, 5, 10;
  @mixin interpolate padding-right, 5, 10;
  @mixin interpolate padding-top, 1.2, 2;
  @mixin interpolate padding-bottom, 1.2, 2;

  margin-top: var(--spacing-lg);
  background-color: var(--color-text);
  color: var(--color-primary);
}

.Signup__brochure-download {
  padding-top: 5em;
}

.Signup__brochure-icon {
  margin-top: var(--spacing-lg);
  margin-right: 3em;
  width: 7%;
}

.Signup__developments {
  display: flex;
  justify-content: flex-start;
  align-items: center;
  gap: 2em;
}

.Signup__developments a {
  align-items: flex-start;
  justify-content: center;
}

.Signup__developments img {
  width: 70%;
  align-items: flex-start;
}
</style>
