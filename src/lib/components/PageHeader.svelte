<script>
export let pageTitle;
export let pageDescription;
export let bgColor;
export let flexContent = false;
</script>
<!-- Header -->
<header class={`${bgColor} p-8 text-center`}>
<!-- Title -->
  <h1 class=" text-3xl lg:text-5xl font-semibold">{pageTitle}</h1>

<!-- Description -->
  <p class=" text-lg bg:text-xl">{pageDescription}</p>
  <!-- Slot for flex content -->
{#if flexContent === true}
  <div class=" bg-white p-4 text-blue-400 rounded-xl max-w-fit">
    <slot />
  </div>
  {/if}
</header>