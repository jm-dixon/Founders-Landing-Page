<template>
  <div class="TheHero">
    <div class="TheHero__top-bar">
      <LogoFoundersPlace class="TheHero__logo" />
    </div>
    <div class="TheHero__inner">
      <div class="TheHero__image">
        <img src="images/hero-image.jpeg">
      </div>
      <div class="TheHero__heading-wrapper">
        <p class="TheHero__coming-soon">
          COMING SOON
        </p>
        <p class="TheHero__heading">
          A PLACE WHERE INNOVATION MEETS INSPIRATION
        </p>
      </div>
      <div class="TheHero__signup-hint">
        <p>
          For updates sign up below
        </p>
        <GraphicTriangle class="TheHero__triangle" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TheHero',
};
</script>

<style lang="postcss" scoped>
@import '~/assets/css/mixins/media';
@import '~/assets/css/settings/media-queries';

.TheHero {
  position: relative;
  display: flex;
  flex-direction: column;
  height: calc(100vh - var(--spacing-md));

  @media (--laptop) {
    height: calc(100vh - var(--spacing-lg));
  }
}

.TheHero__top-bar {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 11rem;

  @media (--laptop) {
    height: 19rem;
  }
}

.TheHero__logo {
  height: 5.5rem;
  color: var(--color-primary);
  margin: 1em;

  @media (--laptop) {
    height: 10.1rem;
  }
}

.TheHero__inner {
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
  flex: 1;
  padding-top: var(--spacing-lg);
  padding-bottom: var(--spacing-lg);
}

.TheHero__image {
  @mixin media;
  @mixin media-full;

  position: absolute;
  top: 0;
  left: 0;
  width: 100%;

  &::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    z-index: 1;
    width: 100%;
    height: 100%;
    background: var(--color-blue);
    mix-blend-mode: multiply;
    opacity: 0.55;
  }
}

.TheHero__heading-wrapper {
  z-index: 1;
  display: flex;
  flex-direction: column;
  row-gap: var(--spacing-3xl);
  text-align: center;
  width: 27rem;
  line-height: 1;
  color: var(--color-white);

  @media (--laptop) {
    row-gap: var(--spacing-xl);
    width: 88.6rem;
    padding-top: 10rem;
  }
}

.TheHero__coming-soon {
  font-size: 3rem;
  filter: drop-shadow(3px 3px 3px #000);

  @media (--laptop) {
    font-size: 6rem;
  }

  @media (--desktop-xl) {
    font-size: 8rem;
  }
}

.TheHero__heading {
  font-size: 4.5rem;
  filter: drop-shadow(3px 3px 3px #000);

  @media (--laptop) {
    font-size: 8rem;
  }

  @media (--desktop-xl) {
    font-size: 10.5rem;
  }
}

.TheHero__signup-hint {
  z-index: 1;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-transform: uppercase;
  color: var(--color-white);
  font-size: 3rem;
}

.TheHero__triangle {
  width: 7rem;
  color: var(--color-secondary);
}
</style>
