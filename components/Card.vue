<template>
  <div class="column">
    <div class="card">
      <header class="card-header">
        <p class="card-header-title has-text-grey">
          {{ title }}
        </p>
      </header>
      <div class="card-content">
        <div class="content has-text-centered">
          <!--<b-icon :icon="icon" size="is-large" type="is-primary" />-->
          <img class="manga-icon" :src="icon" :alt="title" />
        </div>
      </div>
      <footer class="card-footer">
        <div class="card-footer-item">
          <span>
            <slot />
          </span>
        </div>
      </footer>
    </div>
  </div>
</template>

<style>
.manga-icon {
  min-width: 200px;
  height: 300px;
}
</style>

<script>
export default {
  name: 'BuefyCard',
  props: {
    title: {
      type: String,
      required: true,
    },
    icon: {
      type: String,
      required: true,
    },
  },
};
</script>
