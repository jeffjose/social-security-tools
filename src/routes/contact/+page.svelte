<script lang="ts">
  import { AlertCircle, Github, Globe, Mail } from "lucide-svelte";
  import { Rocket } from "radix-icons-svelte";
  import * as Alert from "$lib/components/ui/alert";

  const items = [
    {
      href: "mailto:ggrothau@gmail.com",
      displayName: "ggrothau@gmail.com",
      icon: Mail
    },
    {
      href: "https://gregable.com",
      displayName: "Gregable.com",
      icon: Globe
    },
    {
      href: "https://github.com/gregable/social-security-tools",
      displayName: "Gregable/social-security-tools",
      icon: Github
    }
  ];
</script>

<svelte:head>
  <title>Social Security Calculator - Contact</title>
</svelte:head>

<main class="container">
  <div class="my-10">
    <h1 class="mb-5 text-4xl font-bold tracking-tight">
      Contact the developer
    </h1>
    <div class="w-full sm:w-[30rem]">
      <Alert.Root class="">
        <AlertCircle class="h-4 w-4" />
        <Alert.Title>Heads up!</Alert.Title>
        <Alert.Description
          >For questions about social security benefits, please contact the
          Social Security administration.
        </Alert.Description>
      </Alert.Root>
    </div>
    <p class="leading-7 [&:not(:first-child)]:mt-6 w-full sm:w-1/2">
      I am the right person to answer questions specifically about this site, if
      you spot bugs or have suggestions for things that could be clearer, or
      even just want to say thanks, you can contact me at:
    </p>
    <ul
      class="leading-7 [&:not(:first-child)]:mt-6 gap-2 flex flex-col text-sm w-[16rem]"
    >
      {#each items as item}
        <a
          class="flex gap-2 items-center group hover:text-foreground text-muted-foreground transition border hover:border-foreground/30 rounded"
          href={item.href}
        >
          <div class="bg-foreground/5 group-hover:bg-foreground/10 p-2 rounded">
            <svelte:component this={item.icon} class="w-4 h-4" />
          </div>
          <p class="">{item.displayName}</p>
        </a>
      {/each}
    </ul>
  </div>
</main>
