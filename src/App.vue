<template>
  <div id="app">

    <h4 class="component-title">Colors</h4>
    <Button color="default">color="default"</Button>
    <Button color="primary">color="primary"</Button>
    <Button color="secondary">color="secondary"</Button>
    <Button color="danger">color="danger"</Button>

    <h4 class="component-title">Sizes</h4>
    <Button size="sm">size="sm"</Button>
    <Button size="md">size="md"</Button>
    <Button size="lg">size="lg"</Button>

    <h4 class="component-title">Variants</h4>
    <Button variant="text">variant="text"</Button>
    <Button variant="outline">variant="outline"</Button>

    <h4 class="component-title">Disabled</h4>
    <Button disabled>disabled</Button>

    <h4 class="component-title">Icons</h4>
    <Button startIcon="4k" endIcon="power_settings_new">Hello</Button>

  </div>
</template>

<script>
import Button from '@/components/Button.vue';

export default {
  name: 'App',
  components: {
    Button,
  },
};
</script>

<style lang="scss">
  body {
    background-color: white;
    color: black;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI",
                  Roboto, Helvetica, Arial, sans-serif, "Apple Color Emoji",
                  "Segoe UI Emoji", "Segoe UI Symbol";
  }

  .component-title {
    font-size: 2em;
  }
</style>
