<script lang="ts">
  export let author: string;
  export let publishDate: string;
  export let title: string;
  export let editorialName: string;
</script>

<div>
  <p>{author} ({publishDate}). {title}. {editorialName}.</p>
</div>

<style>
  div {
    padding: 0.125rem 0.25rem;
  }
</style>
