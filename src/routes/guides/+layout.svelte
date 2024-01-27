<script lang="ts">
  import Header2 from "$lib/components/Header2.svelte";
  import GuideFooter from "./guide-footer.svelte";
</script>

<Header2 active="Guides" />
<main>
  <slot />
</main>

<style>
  main {
    max-width: 1080px;
    margin: 0 auto;
  }
</style>
