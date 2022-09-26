<template>
  <div class="Welcome">
    <h1 class="Welcome__heading">Reimagined, redesigned<br>and Revitalised</h1>
    <p class="Welcome__text text-default">
      Set in the heart of the established Stephenson Quarter, adjacent to
      Newcastle upon Tyne's central railway station, with commanding views
      over the River Tyne - Founders Place is a new district of the city
      bringing purpose to its surroundings. It's reimagined, redesigned and
      revitalised in a spirit true to the place's history.
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
  @mixin interpolate padding-top, 5, 10;
  @mixin interpolate padding-bottom, 5, 10;

  width: 100%;
  padding-left: 15%;
  padding-right: 15%;
  background-color: var(--color-secondary);

  @media (--phone-md) {
    padding-left: 8%;
    padding-right: 8%;
  }
}

.Welcome__heading {
  @mixin interpolate margin-bottom, 3, 5;

  color: var(--color-red);
}

.Welcome__text {
  line-height: 1.3;
  color: var(--color-text-secondary);
  margin-top: 8rem;
}

.Welcome__text:not(:first-of-type) {
  margin-top: 2rem;
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
