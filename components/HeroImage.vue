<template>
  <div class="HeroImage">
    <img
      :src="imageDesktop"
      class="HeroImage__image"
    >
    <div class="HeroImage__logo-container">
      <p class="HeroImage__logo-text">
        COMING SOON
      </p>
      <p class="HeroImage__logo-text">
        A PLACE WHERE INNOVATION<br />MEETS INSPIRATION
      </p>
    </div>
  </div>
</template>

<script>
import logoUrl from '~/assets/images/pioneer-logo-01.svg';
import heroImage from '~/assets/images/Newcastle-on-Tyne_ic05522-me.jpeg'

export default {
  name: 'HeroImage',

  data() {
    return {
      imageDesktop: heroImage,
      logoUrlSvg: logoUrl
    };
  },
  computed: {

  }
}
</script>

<style lang="postcss">
@import "~/assets/css/settings/media-queries.css";
@import "~/assets/css/mixins/utils.css";

.HeroImage {
  height: max-content;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.HeroImage__image {
  width: 100%;
  height: auto;
  object-fit: cover;
  max-height: 750px;
}

.HeroImage__logo-container {
  position: absolute;
  padding: 35px;
  width: 50%;
  height: auto;
  top: min(200px, 20vw);
  opacity: 0.9;
}

.HeroImage__logo-container img {
  height: 100%;
}

.HeroImage__logo-text {
  color: var(--color-secondary);
  text-align: center;
  font-size: 4em;
  padding: 1.2em 1em 0.5em 1em;
}
</style>
