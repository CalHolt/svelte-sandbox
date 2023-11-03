<script>
  // import component
    import MessageBox from "../lib/components/messageBox.svelte";
  // Getting rid of document.querySelector
  let test = "testing";

  // rendering html content
  let hello = "<span>is this working?</span>";

  let messsageForBox = {
    title: "generated from object",
    description: "I have rendered this cards text from an object"
  }
</script>
<ul class="m-4 text-center">
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
<!-- writing out each title and description  -->
<MessageBox title="differen box title?" description="this is its own seperate card"/>
<!-- using a made variable to fast track text -->
<MessageBox title = {messsageForBox.title} description = {messsageForBox.description}/>