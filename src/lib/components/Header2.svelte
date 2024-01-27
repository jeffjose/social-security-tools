<script lang="ts">
  export let active = "none";

  let navOptions = [
    { name: "Calculator", link: "calculator", active: false },
    { name: "Guides", link: "guides", active: false },
    { name: "About", link: "about", active: false },
    { name: "Contact", link: "contact", active: false }
  ];
  $: active && navOptions.forEach((o) => (o.active = o.name === active));
</script>

<div
  class="grid sm:grid-cols-[1fr_auto_auto] justify-items-center mb-[10px] w-full sm:mb-5 border-b-[#c5c5c5] border-b border-solid grid-[1fr]"
>
  <h3
    class="leading-10 text-[rgb(150,150,150)] font-medium sm:text-2xl whitespace-nowrap m-0 sm:pl-5 pl-0 text-xl"
  >
    <a class="text-[rgb(150,150,150)]" href="/"
      >SSA.tools Social Security Calculator</a
    >
  </h3>

  <div
    class="text-sm grid grid-cols-[repeat(var(--pill-count),auto)] gap-x-2.5 m-[5px] cursor-pointer
"
    style:--pill-count={navOptions.length.toString()}
  >
    {#each navOptions as option}
      <a
        class="flex noprint text-center align-middle sm:px-[15px] sm:py-2.5 p-[5px] rounded
    {option.active ? 'text-[#fff] bg-[#337ab7]' : ''}
      "
        href="/{option.link}">{option.name}</a
      >
    {/each}
  </div>
  <div class="onlyprint printurl">https://ssa.tools/</div>
</div>

<style>
  @media screen and (max-width: 675px) {
    /**
    * Below 650px the pills and header start to collide, so
    * we move them to separate lines and center.
    */
    .header {
      grid-template-columns: 1fr;
      justify-items: center;
      margin-bottom: 10px;
    }
    h3 {
      padding-left: 0px;
      font-size: 20px;
      line-height: 30px;
    }
    .pill a,
    .pill span {
      padding: 5px 5px;
    }
  }
</style>
