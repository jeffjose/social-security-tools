<script lang="ts">
  import { Header } from "$lib/components/site";
  import GuideFooter from "./guide-footer.svelte";
</script>

<Header />
<main class="container">
  <slot />
</main>
