<script>
  // Import header
  import PageHeader from "../lib/components/PageHeader.svelte";

  let pageTitle = "Home";
  let pageDescription = "This is my SvelteKit Sandbox";

  // --------------------- //
  // MessageBox Importing //
  // --------------------//
  
  // import component
  import MessageBox from "../lib/components/messageBox.svelte";

  // Getting rid of document.querySelector
  let test = "testing";

  // rendering html content
  let hello = "<span>is this working?</span>";

  // Object for text and description of component
  let messsageForBox = {
    title: "generated from object",
    description: "I have rendered this cards text from an object"
  }

  // array, to loop through inside of component 
  let messsagesForBox = [{
    title: "generated from array", description: "first looping description"},
    {title: "second title generated from array", description: "did it work how intended?"
  }]

</script>

<PageHeader {pageTitle} {pageDescription}/>

<!-- attach the variable directly to the html -->

<!-- <h1>SvelteKit Sandbox {@html hello}</h1> -->


<!-- Adding components into the page -->

<!-- Creating differnt cards -->
<MessageBox title="Wow this is cool" description="the description would go here"/>

<!-- writing out each title and description  -->
<MessageBox title="differen box title?" description="this is its own seperate card"/>

<!-- using a made variable to fast track text -->
<MessageBox title = {messsageForBox.title} description = {messsageForBox.description}/>

<!-- Cleanest way to render text to the component using spread operator -->
<MessageBox {...messsageForBox}/>

<!-- Each Loops -->
<h1>Each Loops</h1>
{#each messsagesForBox as box}
<MessageBox {...box}/>
{/each}
