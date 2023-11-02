<script>
  // import component
    import MessageBox from "../lib/components/MessageBox.svelte";
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
<!-- attach component to page -->
<!-- Creating differnt cards -->
<MessageBox title="Wow this is cool" description="the description would go here"/>
<MessageBox title="differen box title?" description="this is its own seperate card"/>