<script>
  // more intuitive name
  export let bgColor;
</script>
<!-- using template literals to allow style to be added to rather than reset after adding a different property -->
<li class={`${bgColor} my-2 text-lg rounded-xl max-w-xs px-4 py-2`}><slot /></li>