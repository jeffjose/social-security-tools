<script lang="ts">
  import { AlertCircle, Github, Globe, Mail } from "lucide-svelte";
  import { Rocket } from "radix-icons-svelte";
  import * as Alert from "$lib/components/ui/alert";
</script>

<svelte:head>
  <title>Social Security Calculator - Contact</title>
</svelte:head>

<main class="container">
  <div class="my-10">
    <h1 class="mb-5 text-4xl font-bold tracking-tight">
      Contact the developer
    </h1>
    <div class="w-[30rem]">
      <Alert.Root class="">
        <AlertCircle class="h-4 w-4" />
        <Alert.Title>Heads up!</Alert.Title>
        <Alert.Description
          >For questions about social security benefits, please contact the
          Social Security administration.
        </Alert.Description>
      </Alert.Root>
    </div>
    <p class="leading-7 [&:not(:first-child)]:mt-6">
      I am the right person to answer questions specifically about this site, if
      you spot bugs or have suggestions for things that could be clearer, or
      even just want to say thanks, you can contact me at:
    </p>
    <ul class="leading-7 [&:not(:first-child)]:mt-6 gap-2 flex flex-col">
      <li class="flex gap-2 items-center">
        <Mail class="w-5" />
        <a href="mailto:ggrothau@gmail.com">ggrothau@gmail.com</a>
      </li>
      <li class="flex gap-2 items-center">
        <Globe class="w-5" />
        <a href="https://gregable.com">Gregable.com</a>
      </li>
      <li class="flex gap-2 items-center">
        <Github class="w-5" />
        <a href="https://github.com/Gregable/social-security-tools">
          Gregable/social-security-tools
        </a>
      </li>
    </ul>
  </div>
</main>
