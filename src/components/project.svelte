<script lang="ts">
  import {
    Accordion,
    AccordionItem,
    ListItem,
    UnorderedList,
  } from "carbon-components-svelte";

  export let link;
  export let name = "";
  export let width = 560;
  export let items = [];
  export let year = "";
  export let links = [];
  export let role = "";
  export let client = "";
  export let iframe = "";
  export let functionalities = [];
  export let tools = [];
  export let image = "";
  export let vimeo = false;

  let innerWidth = 0;
  let innerHeight = 0;

  let gridWidth = 0;

  $: gridWidth = innerWidth / 3;
</script>

<svelte:window bind:innerWidth bind:innerHeight />

<div class="flex justify-between space-x-4 mb-8">
  <div class="flex flex-col justify-between w-full">
    <div class="mb-4">
      <h1 class="text-2xl"><strong>{name}</strong> {client}</h1>
      <h2 class="text-xl">
        {role}{role && year ? ", " + year : year ? year : ""}
      </h2>
      <p class="w-[{width}px]"><slot /></p>
      {#if functionalities.length > 0 || tools.length > 0}
        <div class="grid grid-cols-2">
          {#if functionalities.length > 0}
            <div>
              <h5 class="mt-4">I mostly worked with:</h5>
              <UnorderedList>
                {#each functionalities as functionality}
                  <ListItem>{functionality}</ListItem>
                {/each}
              </UnorderedList>
            </div>
          {/if}
          {#if tools.length > 0}
            <div>
              <h5 class="mt-4">Using:</h5>
              <UnorderedList>
                {#each tools as tool}
                  <ListItem>{tool}</ListItem>
                {/each}
              </UnorderedList>
            </div>
          {/if}
        </div>
      {/if}
    </div>

    <Accordion>
      {#each items as item}
        <AccordionItem title={item}>
          {item}
        </AccordionItem>
      {/each}
      {#if links && links.length > 0}
        <AccordionItem title="Links {links ? '(' + links.length + ')' : ''}">
          <ul>
            {#each links as link}
              <li>
                <a href={link}><p class="w-[300px] truncate">{link}</p></a>
              </li>
            {/each}
          </ul>
        </AccordionItem>
      {/if}
    </Accordion>
  </div>
  {#if link}
    <div class="w-[{gridWidth}px]">
      <iframe
        width={gridWidth}
        height={gridWidth / 1.777777777777778}
        src={"https://www.youtube.com/embed/" + link}
        title="YouTube video player"
        frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
        allowfullscreen
      />
    </div>
  {/if}
  {#if iframe}
    <div class="w-[{gridWidth}px] bg-white">
      <iframe
        width={gridWidth}
        height={gridWidth / 1.777777777777778}
        src={iframe}
        title="skrivunder.fridaysforfuture.se"
        allowfullscreen
      />
    </div>
  {/if}
  {#if image}
    <img src={"/" + image} alt={"Screenshot from " + name} width={gridWidth} />
  {/if}
  {#if vimeo}
    <iframe
      title="vimeo-player"
      src="https://player.vimeo.com/video/74610126?h=866ce837e5"
      width={"100%"}
      frameborder="0"
      allowfullscreen
    />
  {/if}
</div>
