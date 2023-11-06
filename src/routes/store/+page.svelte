<script>
  import ListItem from "../../lib/components/ListItem.svelte";
  // simple array for list 1
  let listItems = ["item 1", "item 2", "item 3", "item 4"];
  // more complex list for list 2
  let secondList = [
    {name: "Joe", species: "Mama",},
    {name: "Moo", species: "Dog",},
  ]
</script>
<h1 class="text-3xl">Store</h1>

<section>
  <h2 class="text-xl">Example list</h2>
  <ul class="list-disc m-4">
    <!-- each loop -->
    {#each listItems as item}
    <ListItem bgColor="bg-purple-300">{item}</ListItem>
    {/each}
  </ul>
</section>

<section>
  <h2 class="text-xl">Example list 2</h2>
  <ul>
    <!-- destructured the list to cut down on code -->
    {#each secondList as {name, species}}
    <!-- selecting our component and also giving it a unique bg color -->
    <ListItem bgColor = "bg-blue-300">{name} is yo {species}</ListItem>
    {/each}
  </ul>
</section>