<script lang="ts">
  import { Sun, Moon, Menu } from "lucide-svelte";
  import { Button } from "$lib/components/ui/button";
  import { toggleMode } from "mode-watcher";
  import { page } from "$app/stores";

  export let active = "none";

  let navOptions = [
    { name: "Calculator", link: "/calculator", active: false },
    { name: "Guides", link: "/guides", active: false },
    { name: "About", link: "/about", active: false },
    { name: "Contact", link: "/contact", active: false }
  ];
  $: active && navOptions.forEach((o) => (o.active = o.name === active));
</script>

<header
  class="supports-[backdrop-filter]:bg-background/60 sticky top-0 z-50 w-full border-b bg-background/95 shadow-sm backdrop-blur"
>
  <div class="flex justify-between h-14 p-5 items-center">
    <div class="gap-5 items-center flex">
      <div class="hidden font-semibold ml-2 md:flex gap-2">
        <svg
          class="w-6 h-6"
          viewBox="0 0 32 34"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M8.86271 33.7051C8.74109 33.5531 8.58907 33.0058 8.54347 32.5041C8.48266 31.9873 8.30024 31.1968 8.11782 30.7559C7.82898 29.9806 7.55534 29.5854 6.00475 27.6547C5.18385 26.621 4.08931 24.3559 3.72447 22.9269C3.35962 21.5436 3.32922 19.5065 3.63325 18.336L3.83088 17.5303L2.99477 16.9982C2.53872 16.6942 1.83943 16.1317 1.44418 15.7212C0.88171 15.1436 0.63848 14.9916 0.364846 15.0524L0 15.1284L0.349644 14.9459C0.577672 14.8243 0.668884 14.6723 0.592874 14.5203C0.182423 13.5018 0.562471 11.9056 1.35297 11.3887C2.12827 10.8718 3.48124 11.7383 3.48124 12.7569C3.48124 13.3649 3.02518 13.9274 2.17387 14.3683C1.85463 14.5355 1.5962 14.7331 1.5962 14.8091C1.5962 14.9611 2.46271 15.5388 3.162 15.8429C4.0285 16.2077 4.21093 16.1013 5.06223 14.7939L5.85273 13.5778L6.71924 14.2923C8.36105 15.63 10.3525 16.3293 12.5416 16.3293C15.1259 16.3293 17.2542 15.4476 19.0936 13.593C20.0209 12.6657 20.3858 12.1488 20.9178 11.0695C21.6931 9.44286 22.0884 8.89559 22.8789 8.34832C23.6238 7.83146 25.0071 7.3602 25.7976 7.3602C26.2689 7.3602 26.4209 7.43621 26.5425 7.72504C26.6793 8.01388 26.6337 8.22671 26.2993 8.89559C26.0257 9.41246 25.8584 10.0509 25.7976 10.6438L25.7368 11.5711L26.9682 12.9241C27.9259 13.9578 28.3667 14.6115 28.9292 15.7516L29.6437 17.2262L30.4798 17.2414C31.9848 17.2414 32 17.2718 32 20.3578C32 23.4438 31.9848 23.4742 30.4798 23.4742H29.6437L29.3853 24.2039C28.914 25.4809 28.0019 26.8338 26.5577 28.3692C24.9159 30.1022 24.5511 30.8167 24.4447 32.4433C24.3838 33.2338 24.2926 33.6443 24.1254 33.7811C23.9582 33.9027 23.1677 33.9635 21.4347 33.9635C18.6223 33.9635 18.4703 33.9027 18.4703 32.7778V32.1393H17.0717C16.2964 32.1393 15.3995 32.0937 15.0955 32.0481L14.5178 31.9417V32.793C14.5178 33.4771 14.457 33.6747 14.229 33.8115C14.0618 33.9027 12.8912 33.9635 11.5078 33.9635C9.39478 33.9635 9.06033 33.9331 8.86271 33.7051ZM25.7824 17.1046C26.3145 16.5573 26.3449 16.0405 25.8584 15.478C25.5848 15.1588 25.372 15.0524 24.9311 15.0524C23.9582 15.0524 23.2741 16.2381 23.8366 16.9526C24.3838 17.6519 25.1743 17.7127 25.7824 17.1046ZM2.61473 13.6234C2.91877 13.3497 2.97957 13.1825 2.88836 12.8633C2.64513 11.8296 1.50499 11.5255 1.06413 12.3768C0.775297 12.9393 0.775297 13.4866 1.06413 14.0642L1.30736 14.5203L1.76342 14.2467C2.02185 14.0946 2.4019 13.821 2.61473 13.6234Z"
            fill="url(#paint0_linear_1_12)"
          />
          <path
            d="M10.7173 14.1402C9.42516 13.7754 8.51305 13.2281 7.50972 12.24C3.90687 8.62195 5.00141 2.73881 9.68359 0.595347C13.5449 -1.16807 18.3791 1.15782 19.4584 5.30794C20.4617 9.19962 18.1815 13.0913 14.2898 14.1402C13.3625 14.3987 11.6294 14.3987 10.7173 14.1402Z"
            fill="url(#paint1_linear_1_12)"
          />
          <defs>
            <linearGradient
              id="paint0_linear_1_12"
              x1="4.625"
              y1="10.7871"
              x2="22.5234"
              y2="38.9017"
              gradientUnits="userSpaceOnUse"
            >
              <stop stop-color="#2AF598" />
              <stop offset="1" stop-color="#009EFD" />
            </linearGradient>
            <linearGradient
              id="paint1_linear_1_12"
              x1="7.44031"
              y1="1.84644"
              x2="17.7179"
              y2="15.2589"
              gradientUnits="userSpaceOnUse"
            >
              <stop stop-color="#2AF598" />
              <stop offset="1" stop-color="#009EFD" />
            </linearGradient>
          </defs>
        </svg>

        <a href="/">ssa.tools</a>
      </div>
      <nav class="flex items-center gap-6 text-sm">
        {#each navOptions as option}
          <a
            href={option.link}
            class="transition-colors hover:text-foreground/80 {$page.url
              .pathname == option.link
              ? 'text-foreground'
              : 'text-foreground/60'}">{option.name}</a
          >
        {/each}
      </nav>
    </div>
    <div class="text-foreground/60 hover:text-foreground/80 transition-colors">
      <!--mid -->
    </div>
    <div>
      <Button variant="ghost" on:click={toggleMode} size="icon">
        <Sun
          class="h-[1.2rem] w-[1.2rem] rotate-0 scale-100 transition-all dark:-rotate-90 dark:scale-0"
        />
        <Moon
          class="absolute h-[1.2rem] w-[1.2rem] rotate-90 scale-0 transition-all dark:rotate-0 dark:scale-100"
        />
        <span class="sr-only">Toggle theme</span>
      </Button>
    </div>
  </div>
</header>
