<script lang="ts">
  export let title: string;
</script>

<li>
  <h4>{title}</h4>
  <slot />
</li>

<style>
  li {
    margin-top: 1rem;
    padding-block: 0.5rem;
  }
  li > :global(*:not(h4)) {
    padding-block: 0.5rem;
    padding-inline: 1rem;
  }
</style>
