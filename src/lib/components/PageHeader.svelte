<script>
export let pageTitle;
export let pageDescription;
</script>
<!-- Header -->
<header class=" bg-blue-200 p-8 text-center">
<!-- Title -->
  <h1 class=" text-3xl lg:text-5xl font-semibold">{pageTitle}</h1>

<!-- Description -->
  <p class=" text-lg bg:text-xl">{pageDescription}</p>
  <!-- Slot for flex content -->
  <div class=" bg-white">
    <slot />
  </div>
</header>