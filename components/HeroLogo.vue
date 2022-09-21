<template>
  <div class="HeroLogo">
    <div class="HeroLogo__logo-wrapper">
      <img :src="logoUrl" class="HeroLogo__logo-img">
      <h3 class="HeroLogo__coming-soon">Coming Soon</h3>
    </div>
  </div>
</template>

<script>
import FoundersPlaceLogoUrl from '@/assets/images/founders-place-logo-01-01.svg';

export default {
  name: 'HeroLogo',

  data() {
    return {
      logoUrl: FoundersPlaceLogoUrl,
    };
  },

  computed: {
    isDesktopLg() {
      return this.$store.state.isDesktopLg;
    },
  },

  watch: {
    isDesktopLg: {
      handler(newVal) {
        this.textureImgUrl = newVal ? this.textureUrl : this.textureHorizUrl;
      },
      immediate: true,
    },
  },
}
</script>

<style lang="postcss">
@import "~/assets/css/settings/media-queries.css";
@import "~/assets/css/mixins/utils.css";

.HeroLogo {
  display: flex;
  background-color: var(--color-secondary);
  color: white;
  height: auto !important;
  justify-content: center;
  align-items: center;

  @media (--desktop-lg) {
    flex-direction: row;
  }
}

.HeroLogo__logo-wrapper {
  display: flex;
}

.HeroLogo__logo-img {
  @mixin interpolate padding-top, 3, 4;
  @mixin interpolate width, 10, 20;
}

.HeroLogo__texture-img {
  width: 100%;
  height: 8%;
  object-fit: cover;

  @media (--desktop-lg) {
    width: 7%;
    height: 100%;
  }
}

.HeroLogo__coming-soon {
  @mixin interpolate font-size, 2, 2.5;

  margin-top: var(--spacing-lg);
  margin-bottom: var(--spacing-lg);
  color: var(--color-lighter-orange);

  @media (--desktop-lg) {
    font-size: 3.5rem;
    margin-top: 7rem;
    margin-bottom: 0;
  }
}
</style>
