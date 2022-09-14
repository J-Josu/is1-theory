<script lang="ts">
  export let height: string;
</script>

<div style="--height:{height};">
  <span class="code">&lt;</span><span class="text">s</span>
  <img src="/argentinian_flag_sun.svg" alt="" />
  <span class="text">l</span>
  <span class="dev">dev</span>
  <span class="code">/&gt;</span>
</div>

<style>
  div {
    display: flex;
    justify-content: center;
    padding: calc(var(--height) / 4);
    line-height: var(--height);
    font-size: var(--height);
    font-weight: 900;
    font-family: monospace;
    text-transform: uppercase;
    --shadow-size: 0px;
    --dev-color: inherit;
  }
  div:hover {
    --dev-color: hsl(200, 100%, 50%);
  }
  img {
    height: var(--height);
    transition: filter 1s ease-in;
    filter: drop-shadow(0px 0px var(--shadow-size) hsl(45, 100%, 50%));
  }
  img:hover {
    --shadow-size: calc(var(--height) / 4);
  }
  .dev {
    rotate: y 180deg;
    color: var(--dev-color);
    transition: color 0.5s ease-in;
  }
  @media screen and (max-width: 688px) {
    .text {
      display: none;
    }
    .dev {
      color: hsl(200, 100%, 50%);
    }
  }
</style>
