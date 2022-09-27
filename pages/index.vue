<template>
  <div class="Home">
    <div class="Home__body grid">
      <div>
        <Welcome />
      </div>
      <div class="Home__signup-form">
        <SignupForm />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
}
</script>

<style lang="postcss">
@import "~/assets/css/settings/media-queries.css";
@import "~/assets/css/mixins/utils.css";

.Home {
  /* padding-top: var(--spacing-md);
  padding-bottom: 7.5rem;

  @media (--laptop) {
    padding-top: var(--spacing-2xl);
    padding-bottom: var(--spacing-2xl);
  } */
}

.Home__body {
  --grid-row-gap: var(--spacing-xl);

  /* padding-top: var(--spacing-md);
  padding-bottom: 7.5rem; */

  @media (--laptop) {
    --grid-columns: 2;
    --grid-column-gap: 0;

    /* padding-top: var(--spacing-2xl);
    padding-bottom: var(--spacing-2xl); */
  }

  & > * {
    padding-top: var(--spacing-md);

    @media (--laptop) {
      padding-top: var(--spacing-2xl);
      padding-bottom: var(--spacing-2xl);
    }
  }
}

.Home__signup-form {
  display: flex;
  align-items: center;
  justify-content: center;
  background: var(--color-primary);
}
</style>
