<script>
  import PageHeader from "../../lib/components/PageHeader.svelte";
  
  const pageTitle = "Gallery";
  const pageDescription = "This is a gallery of all living proof of bigfoot";
  let bgColor = "bg-red-500";

  // simple logic for login to work
  let login = true;
  // output functions to show its working
  function loginGranted(e) {
    if (login === true){
      alert("Login granted");
    } else {
      alert("SELF DESTRUCTION COMMENCING");
    }
  }
  // changing login value to show else value of function
  function toggleLogin(e) {
    login = !login;
  }
 
  let name = "Cal";


</script>
<PageHeader {pageTitle} {pageDescription} {bgColor} flexContent>Hello</PageHeader>

{#if name === "Cal"}
<!-- Alert button -->
<button on:click={loginGranted} class = "rounded-md bg-green-500 px-4 py-2 mx-4 text-white transition duration-350 hover:bg-red-700 my-4">Send Alert</button>
<!-- Toggle button -->
<button on:click={toggleLogin} class="rounded-md bg-purple-500 px-4 py-2 mx-4 text-white transition duration-350 hover:bg-red-700 my-4">Toggle</button>
<!-- Showing status of login -->
<p>value of login: {login}</p>
{/if}