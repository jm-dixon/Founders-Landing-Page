<template>
  <div class="Welcome">
    <h2 class="Welcome__heading">Founders Place is being reimagined, redesigned and revitalised.</h2>
    <p class="Welcome__text text-default">
    Set in the heart of the established Stephenson Quarter, Founders Place has a long history as a melting pot for creative thinkers, entrepreneurial mavericks and visionary leaders. Once George and Robert Stephenson’s powerhouse of innovation in the industrial era, now the revolution is one of sustainable design, life-enhancing technologies, human wellbeing and urban greening.
    <br><br>
    Whether you are looking for a place to explore and have fun, build a home or base your business, Founders Place is bringing together leading architects, designers and the best sustainable technologies, to put the quality of human experience at its absolute heart.
    <br><br>
    <span class="text-default-bold">Come and join us, find out more…</span>
    </p>
  </div>
</template>

<script>
import phoneIcon from '~/assets/images/THE PATTERNSHOP-Icon-Telephone-RGB.svg';
import emailIcon from '~/assets/images/THE PATTERNSHOP-Icon-Mail-RGB.svg';

export default {
  name: 'Welcome',
  data() {
    return {
      icons: {
        phoneIconUrl: phoneIcon,
        emailIconUrl: emailIcon
      }
    }
  }
}
</script>

<style lang="postcss">
@import "~/assets/css/settings/media-queries.css";
@import "~/assets/css/mixins/utils.css";

.Welcome {
  /* @mixin interpolate padding-top, 5, 10;
  @mixin interpolate padding-bottom, 5, 10; */

  display: flex;
  flex-direction: column;
  row-gap: var(--spacing-xl);
  width: 100%;
  padding-left: 15%;
  padding-right: 15%;

  @media (--phone-md) {
    padding-left: 8%;
    padding-right: 8%;
  }
}

.Welcome__heading {
  font-size: 6rem;
  line-height: 1;
  color: var(--color-red);
  margin-top: 1em;

  @media (--tablet) {
    margin-top: 0;
  }

  @media (--laptop) {
    font-size: 8rem;
    margin-top: 0;
  }
}

.Welcome__text {
  line-height: 1.3;
  color: var(--color-text-secondary);
}

.Welcome__icons {
  width: 100%;
  margin-top: 2em;
}

.Welcome__grid {
  display: grid;
  grid-template-columns: 3% 97%;
  column-gap: 10px;
  margin: 1em 0 1em 0;
}

.Welcome__grid p {
  margin-top: 0.5em;
}

</style>
