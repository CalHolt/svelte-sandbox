<script>

  // Getting rid of document.querySelector
  let test = "testing";

  // rendering html content
  let hello = "<span>is this working?</span>";
</script>
<ul>
  <li class="text-sky-500">
      <a href="/gallery">Gallery</a>
  </li>
  <li class="text-red-500">
    <a href="/store">Store</a>
  </li>
  <li class="text-yellow-500">
    <a href="/contact">Contact</a>
  </li>
</ul>
<!-- attach the variable directly to the html -->
<h1>SvelteKit Sandbox {@html hello}</h1>

