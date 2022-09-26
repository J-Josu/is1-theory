<script lang="ts">
  export let surnameName: string;
  export let publishDate: string;
  export let title: string;
  export let siteName: string;
  export let siteURL: string;
</script>

<div>
  <p>{surnameName}. ({publishDate}). {title}. {siteName}.</p>
  <a href={siteURL} target="_blank" rel="noopener noreferrer">{siteURL}</a>
</div>

<style>
  div {
    padding: 0.125rem 0.25rem;
  }
  a {
    color: var(--color-dark-blue);
    font-weight: 500;
  }
</style>
