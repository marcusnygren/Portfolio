<script lang="ts">
  import {
    StructuredList,
    StructuredListHead,
    StructuredListRow,
    StructuredListCell,
    StructuredListBody,
    StructuredListInput,
  } from "carbon-components-svelte";
  import CheckmarkFilled from "carbon-icons-svelte/lib/CheckmarkFilled.svelte";

  let clickedIndex = null;

  function handleClick(e) {
    let clicked = e.currentTarget.getAttribute("for");
    clickedIndex = clicked.split("-")[1];
  }

  let items = [
    {
      id: 0,
      paper:
        "Developing a Mobile Learning Application for Entrepreneurship Education in Uganda and Zambia",
      area: "Master thesis",
      keywords:
        "co-design, web, UX, entrepreneurship, edtech, design for learning",
      link: "https://www.diva-portal.org/smash/record.jsf?pid=diva2%3A1018544&dswid=1799",
      year: "2016",
      images: ""
    },
    {
      id: 1,
      paper: "Shader Creation Case Study: Is Visual Programming The Future?",
      area: "3D Computer Graphics course",
      keywords:
        "Unity, shader programming, visual scripting, OpenGL, GLSL, WebGL, standard shader, Shader Forge",
      link: "shader_creation_case_study.pdf",
      year: "2015",
      images: ["shaderforge_halftoneshader.png", "shaderforge_earth.png"],
    },
    {
      id: 2,
      paper: "Championing diversity at events via D3.js and the Eventbrite API",
      area: "Information visualization",
      keywords:
        "D3.js, API, Multivariate data, Plot, Bar chart, Slider, Age distribution",
      link: "https://drive.google.com/file/d/0BzlK1PD8EE75RjBLQzREczNMVnc/view?usp=sharing&resourcekey=0-7PqmalDodCK4GFRt5XRa6A",
      year: "2015",
      images: [],
    },
    {
      id: 3,
      paper: "Badges for learning",
      area: "Gamification",
      keywords: "gamification, badges, learning, education, edtech",
      link: "https://www.coderdojonkpg.se/koda.html#badges",
      year: "2017"
    }
  ];
</script>

<StructuredList>
  <StructuredListHead>
    <StructuredListRow head>
      {#each Object.keys(items[0]) as column}
        <StructuredListCell head
          >{column[0].toUpperCase() + column.slice(1)}</StructuredListCell
        >
      {/each}
      <StructuredListCell head>{""}</StructuredListCell>
    </StructuredListRow>
  </StructuredListHead>
  <StructuredListBody>
    {#each items as item}
      <StructuredListRow on:click={handleClick} label for="row-{item.id}">
        {#each Object.values(item) as column}
          <StructuredListCell>{column}</StructuredListCell>
        {/each}
        <StructuredListInput
          id="row-{item}"
          value="row-{item}-value"
          title="row-{item}-title"
          name="row-{item}-name"
        />
        <StructuredListCell>
          <CheckmarkFilled
            class="bx--structured-list-svg"
            aria-label="select an option"
            title="select an option"
          />
        </StructuredListCell>
      </StructuredListRow>
    {/each}
  </StructuredListBody>
</StructuredList>

{#if clickedIndex}
  <h2>{items[clickedIndex].paper}</h2>
  <a href={items[clickedIndex].link}>{items[clickedIndex].link}</a>
  {#each items[clickedIndex].images as image}
    <a href={image}><img class="mb-2" src={image} /></a>
  {/each}
{/if}
