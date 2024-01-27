<script lang="ts">
  import "$lib/global.css";
  import { page } from "$app/stores";
  import { browser } from "$app/environment";
  import posthog from "posthog-js";
  import { ModeWatcher } from "mode-watcher";

  $: $page.url.pathname, browser && posthog.capture("$pageview");
</script>

<ModeWatcher defaultMode={"light"} />

<slot />
