<script lang="ts" context="module">
  //IMPORT components
  import Tile from "./Tile.svelte";

  //IMPORT images
  import linkIcon from "$lib/images/link.png";

  //DB .
  export const tiles = [
    {
      label: "Code editor",
      description:
        "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Tempora quibusdam officiis soluta suscipit harum quam animi modi! Consequuntur accusantium, molestiae vero laudantium ducimus error esse et voluptatem dolorum rem dicta!",
      link: "code_editor",
      local: true,
    },
    {
      label: "Example #2",
      description:
        "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Tempora quibusdam officiis soluta suscipit harum quam animi modi! Consequuntur accusantium, molestiae vero laudantium ducimus error esse et voluptatem dolorum rem dicta!",
      link: "https://example.com/",
      local: false,
    },
    {
      label: "Example #3",
      description:
        "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Tempora quibusdam officiis soluta suscipit harum quam animi modi! Consequuntur accusantium, molestiae vero laudantium ducimus error esse et voluptatem dolorum rem dicta!",
      link: "https://example.com/",
      local: false,
    },
  ];
</script>

<div>
  <section
    class="flex flex-col realtive text-white font-semibold space-y-2 mx-[10%] transition-all"
    id="creations"
  >
    <h1
      id="sectionHeader"
      class="w-fit flex flex-row -ml-9 gap-3 mb-2 lg:text-3xl text-2xl lg:hover:underline lg:hover:tracking-widest transition-all"
    >
      <a href="#creations" class="self-center">
        <img
          src={linkIcon}
          class="opacity-0 text-base transition-all duration-100 relative h-5"
          alt="link icon"
          id="sectionLinkIcon"
        />
      </a>
      Creations
    </h1>
  </section>

  <tiles class="flex flex-row flex-wrap justify-evenly w-full mr-[5%] relative">
    {#each tiles as tile}
      <Tile
        label={tile.label}
        description={tile.description}
        link={tile.link}
      />
    {/each}
  </tiles>
</div>

<style>
  @media only screen and (min-width: 1024px) {
    #sectionHeader:hover #sectionLinkIcon {
      opacity: 1;
    }
  }
</style>
