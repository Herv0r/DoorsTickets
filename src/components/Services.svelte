<script>
  import { Card } from "framework7-svelte";

  let services = [
    {
      id: 1, 
      title: "Header 1",
      content: "Card with header and footer. Card headers are used to display card titles and footers for additional information or just for custom actions.",
      footer: "Footer 1"
    },
    {
      id: 2,
      title: "Header 2",
      content: "Card with header and footer. Card headers are used to display card titles and footers for additional information or just for custom actions."
    },
    {
      id: 3, 
      title: "Header 3",
      content: "Card with header and footer. Card headers are used to display card titles and footers for additional information or just for custom actions.",
      footer: "Footer 3"
    }
  ];
</script>

<section>
  <h1 class="card-text">¿Qué servicios brindamos?</h1>
  <div class="cards">
    {#each services as service (service.id)}
      <Card raised class="card" title={service.title} content={service.content} footer={service.footer} />
    {/each}
  </div>
</section>

