<script lang="ts">
  export let title: string;
</script>

<div class="container">
  <h3>{title}:</h3>
  <slot />
</div>

<style>
  .container {
    position: relative;
    border-bottom: 2px solid gray;
    padding-block: 1rem;
    margin-bottom: 1rem;
  }
  .container::before {
    content: '';
    width: 110%;
    height: 105%;
    position: absolute;
    top: -2.5%;
    left: -5%;
    background-color: hsla(0, 0%, 60%, 0.1);
    box-shadow: 0 0 10px 10px hsla(0, 0%, 60%, 0.1);
  }
</style>
