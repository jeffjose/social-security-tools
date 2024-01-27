<script lang="ts">
  import { Header } from "$lib/components/site";
  import GuideFooter from "./guide-footer.svelte";
</script>

<Header />
<main>
  <slot />
</main>

<style>
  main {
    max-width: 1080px;
    margin: 0 auto;
  }
</style>
