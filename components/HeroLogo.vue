<template>
  <div class="HeroLogo">
    <div class="HeroLogo__logo-wrapper">
      <LogoFoundersPlace />
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
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 11rem !important;

  @media (--laptop) {
    height: 12.5rem !important;
  }

  @media (--desktop-lg) {
    flex-direction: row;
    height: 14rem;
  }
}

.HeroLogo__logo-wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
}

.HeroLogo__logo-img {
  @mixin interpolate padding-top, 3, 4;
  @mixin interpolate width, 10, 20;

  padding: 0;
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
