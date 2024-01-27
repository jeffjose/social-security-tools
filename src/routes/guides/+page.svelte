<script lang="ts">
  import { Badge } from "$lib/components/ui/badge";

  import blurbs from "./blurbs.json";
</script>

<svelte:head>
  <title>Social Security Calculator - Guides</title>
</svelte:head>

<div>
  <h1 class="mt-10 mb-5 text-4xl font-bold tracking-tight">Guides</h1>
  <ul class="flex flex-wrap gap-2">
    {#each blurbs as blurb}
      <li
        class="min-w-[20rem] w-[40rem] border rounded-xl p-5 hover:border-foreground/50 hover:bg-muted/30 transition"
      >
        <a href={blurb.href}>
          <div class="flex flex-col gap-1 justify-start">
            <p class="text-xs text-muted-foreground">
              {blurb.date.toUpperCase()}
            </p>
            <h3 class="text-xl font-semibold tracking-tight">{blurb.title}</h3>
          </div>
          <p class="leading-7 [&:not(:first-child)]:mt-3 text-muted-foreground">
            {blurb.description}
          </p>
        </a>
      </li>
    {/each}
  </ul>
</div>
