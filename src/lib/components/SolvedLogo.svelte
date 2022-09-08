<script lang="ts">
  export let height: string;
</script>

<div style="--height:{height};">
  <span>&lt;s</span>
  <img src="/argentinian_flag_sun.svg" alt="" />
  <span>l</span>
  <span class="inverted">dev</span>
  <span>/&gt;</span>
</div>

<style>
  div {
    font-size: var(--height);
    text-transform: uppercase;
    display: flex;
    justify-content: center;
    line-height: var(--height);
    font-weight: 900;
    font-family: monospace;
    --shadow-size: 0px;
    padding: calc(var(--height) / 4);
  }
  img {
    height: var(--height);
    transition: filter 1s ease-in;
    filter: drop-shadow(0px 0px var(--shadow-size) hsl(45, 100%, 50%));
  }
  img:hover {
    --shadow-size: 16px;
  }
  .inverted {
    rotate: y 180deg;
  }
</style>
