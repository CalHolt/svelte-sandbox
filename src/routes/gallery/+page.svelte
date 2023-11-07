<script>
  import PageHeader from "../../lib/components/PageHeader.svelte";
  
  const pageTitle = "Gallery";
  const pageDescription = "This is a gallery of all living proof of bigfoot"
  let bgColor = "bg-red-500";
</script>
<PageHeader {pageTitle} {pageDescription} {bgColor} flexContent>Hello</PageHeader>
