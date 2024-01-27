<script lang="ts">
  import { HandCoins, Heart, Mail, Palmtree, TrendingUp } from "lucide-svelte";

  const whatifs = [
    {
      icon: HandCoins,
      description:
        "What happens to my benefit if I earn additional wages for several more years?"
    },
    {
      icon: TrendingUp,
      description:
        "How does my benefit change as my total earnings grow during my lifetime?"
    },
    {
      icon: Palmtree,
      description:
        "What happens if I choose to take my benefits early? What if I delay and take them late?"
    },
    {
      icon: Heart,
      description:
        "How are my benefits affected by my spouse's earnings records, and vice versa."
    }
  ];

  const contributors = [
    {
      initials: "GG",
      name: "Greg Grothaus",
      description:
        "Greg is the primary developer of this site. He is a software engineer who has worked on this project on the side for several years.",
      href: "gregable.com"
    },
    {
      initials: "SK",
      name: "Sotirios Keros",
      description:
        "Sotirios Keros a physician, financial planner, and co-founder of the not-for-profit Doctored Money. Sotirios contributed heavily to the design and correctness of the calculations this tool makes."
    },
    {
      initials: "SN",
      name: "Steve Nicolai",
      description:
        "Steve Nicolai a semi-retired telecom software engineer. Steve contributed the implementation of social security credits."
    }
  ];
</script>

<svelte:head>
  <title>Social Security Calculator - About</title>
</svelte:head>

<main class="container">
  <div class="my-10">
    <h1 class="mt-10 mb-5 text-4xl font-bold tracking-tight">
      About ssa.tools - The Social Security Calculator
    </h1>
    <p class="leading-7 [&:not(:first-child)]:mt-6">
      This site provides individuals with an estimate of their future Social
      Security retirement benefits. The benefits are based on the earnings
      record provided by the Social Security Administration. A detailed report
      is created from this data.
    </p>
    <h3
      class="font-heading mt-12 scroll-m-20 border-b pb-2 text-2xl font-semibold tracking-tight first:mt-0"
    >
      What If?
    </h3>
    <p class="leading-7 [&:not(:first-child)]:mt-6">
      This site provides clear interactive visuals that let the user investigate
      how different choices might affect their overall benefit. Scenarios
      include:
    </p>
    <ul class="leading-7 [&:not(:first-child)]:mt-6 flex flex-wrap gap-2">
      {#each whatifs as whatif}
        <div
          class="w-1/3 rounded text-muted-foreground transition border flex items-center justify-center flex-col p-8 gap-5 hover:bg-foreground/5 hover:border-foreground/50 hover:text-foreground"
        >
          <div class="p-5 bg-foreground/5 rounded-full">
            <svelte:component this={whatif.icon} class="h-10 w-10" />
          </div>
          <p class="text-sm text-center">
            {whatif.description}
          </p>
        </div>
      {/each}
    </ul>

    <h3
      class="font-heading mt-12 scroll-m-20 border-b pb-2 text-2xl font-semibold tracking-tight first:mt-0"
    >
      Security
    </h3>
    <p class="leading-7 [&:not(:first-child)]:mt-6">
      This site does not store any data entered by users. All calculations are
      made client-side in the browser's JavaScript and are never transmitted
      over the internet.
    </p>
    <p class="leading-7 [&:not(:first-child)]:mt-6">
      While unnecessary for security, this can be confirmed by loading the site
      in your browser, and then disconnecting your computer before entering any
      additional data.
    </p>
    <h3
      class="font-heading mt-12 scroll-m-20 border-b pb-2 text-2xl font-semibold tracking-tight first:mt-0"
    >
      Accuracy
    </h3>
    <p class="leading-7 [&:not(:first-child)]:mt-6">
      This site should be correct, and I will update it as Social Security rules
      change. However, there are no <i>guarantees</i> of the accuracy of this information.
      It should be treated as a useful exploratory tool, but any decisions should
      be made after researching the subject yourself.
    </p>
    <p class="leading-7 [&:not(:first-child)]:mt-6">
      The site was most recently updated on Oct 12, 2023 with the latest 3.2%
      COLA adjustment.
    </p>
    <h3
      class="font-heading mt-12 scroll-m-20 border-b pb-2 text-2xl font-semibold tracking-tight first:mt-0"
    >
      Why?
    </h3>
    <p class="leading-7 [&:not(:first-child)]:mt-6">
      This site is completely free and contains no advertising. I don't collect
      your email address, subscribe you to SMS services, make a credit report
      inquiry, kill a dolphin, etc. Feel free to use the site without wondering
      if there is a catch.
    </p>
    <p class="leading-7 [&:not(:first-child)]:mt-6">
      Costs for running the site are minimal, just a few dollars a year, plus my
      time.
    </p>
    <p class="leading-7 [&:not(:first-child)]:mt-6">
      I noticed that most people don't understand their Social Security benefits
      very well. The online tools at SSA.gov are excellent, but I felt lacking
      in a few places. In particular, I felt that by simply spitting out a final
      number, the results failed to educate the user as to how the program
      works. I thought it would be useful to contribute a tool that helped folks
      to understand their own Social Security benefit and how it will help them
      in the future.
    </p>
    <p class="leading-7 [&:not(:first-child)]:mt-6">
      The <a href="/contact">author of this site</a> could never have done all of
      this without help from the internet. This page lists some of the contributors
      that have made this all possible.
    </p>
    <h3
      class="font-heading mt-12 scroll-m-20 border-b pb-2 text-lg font-semibold tracking-tight first:mt-0"
    >
      Major Contributors
    </h3>
    <div class="flex flex-col gap-2 mt-2">
      {#each contributors as contributor}
        <div class="w-[30rem] bg-background/20 rounded-lg border p-5">
          <div class="flex items-center gap-2">
            <div
              class="rounded-full h-10 w-10 bg-red-500 items-center justify-center flex font-semibold"
            >
              {contributor.initials.toUpperCase()}
            </div>
            <p class="font-semibold">{contributor.name}</p>
          </div>
          <div class="mt-4">
            {contributor.description}
          </div>
        </div>
      {/each}
    </div>

    <h3
      class="font-heading mt-12 scroll-m-20 border-b pb-2 text-2xl font-semibold tracking-tight first:mt-0"
    >
      Contributions Welcome
    </h3>
    <p class="leading-7 [&:not(:first-child)]:mt-6">
      If you would like to contribute, the project is on github at:
      <a href="https://github.com/Gregable/social-security-tools">
        Gregable/social-security-tools
      </a>. Please file issues in the
      <a href="https://github.com/Gregable/social-security-tools/issues">
        Issue Tracker
      </a>.
    </p>
  </div>
</main>
