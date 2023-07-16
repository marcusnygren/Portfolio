<script lang="ts">
  import { Accordion, AccordionItem } from "carbon-components-svelte";
  import { UnorderedList, ListItem } from "carbon-components-svelte";

  let jobs = [
    {
      name: "Norconsult Digital",
      role: "UI Programmer & UX Designer",
      year: "2022-2023",
      link: "http://norconsultdigital.se",
      description:
        "Building the next version of a web platform for dialogue between municipalities, entrepreneurs and citizens. Also UX designer and lead frontend developer for our citizen portal in Svelte. The result was a user-friendly AA WCAG 2.1-approved platform with automated self-service tools. Also: leadership, teaching, facilitating workshops, onboarding new colleagues, client dialogue.",
      skills:
        "Svelte, Playwright, Storybook, TypeScript, JavaScript, HTML, CSS, UX, UI, Figma, CI/CD, Docker",
    },
    {
      name: "Telia",
      role: "UI Programmer & UX Designer",
      year: "2019-2022",
      link: null,
      description:
        "I was design lead and frontend developer together with a very talented group of developers, designers and leaders. I got involved all the way from proof of concept for the investment pitch, to launching 1.0+. I specialized in design methodology, building features, and UI programming. The tool quickly became increasingly appreciated by stakeholders and users, thanks to quick feedback, co-design with users, and meeting real needs. I introduced Figma. Code conversion from jQuery to React, OpenLayers 2 into 6. Also: JavaScript, HTML, SASS, Java. ",
      skills: "React, JavaScript, Storybook, D3.js, Figma, UX, UI, Java",
    },
    {
      name: "Edvira",
      role: "CTO & Consultant & Educator",
      year: "2016-",
      link: null,
      description:
        "Co-founded an impact edtech company focusing on inclusive programming in schools, with our methodology teaching code to more than 100 000 Swedish pupils in our first 4 months. Often used the MEAN stack, being full-stack. I co-designed and co-developed multiple edtech solutions for municipalities and edtech startups, e.g. “PlayIT”, the world’s first Internet of Things-powered playground for kids, together with KTH, Uppsala university, Ecorado and Linköping.",
      skills:
        "React, Node, Express, mongoDB, responsive design, interaction design, CI/CD",
    },
    {
      name: "Spotify",
      role: "Project Leader",
      year: "2012-2013",
      link: null,
      description:
        "Project leader within the team dedicated to making Spotify the best place to be as an engineer. Various internal projects within Technology.",
      skills:
        "Leadership, Agile, Clean Code Practices, Pair Programming, Code Refactoring, Design Patterns, TDD, CI/CD, Engineering Culture, Organizational Change",
    },
    {
      name: "SACC-USA",
      role: "Digital Media & Web",
      year: "2012-2013",
      link: "http://sacc-usa.org",
      description:
        "Solely built a WordPress Multisite totalling 17 connected sites, HTML/CSS/PHP/MySQL and UX/UI design. 6-month full-time internship during my university studies, headhunted via LinkedIn.",
      skills: "HTML/CSS, PHP/MySQL, WordPress, UX, UI",
    },
    {
      name: "Marcus Nygren AB",
      role: "Freelance in Web & Graphic Design",
      year: "2007-2017",
      link: null,
      description:
        "Started doing lots of HTML/WordPress sites and graphic design for small businesses in parallel to my studies. Later I took on larger web, design & leadership projects. Consulted for example in Seattle, U.S., at app engineering agency Assemble, and Swedish e-commerce agency HyperLab.",
      skills:
        "React (since 2014), iOS/Android, design tools, WordPress, project management, HTML, CSS, PHP, mySQL, JavaScript, UX, UI",
      projects: [
		"Swedish Championships in Orienteering (Adobe Illustrator)",
		"Rim Mourad Karate Champion (HTML/CSS/WordPress)", /* https://web.archive.org/web/20160329004050/http://rimmourad.se/ */
        "Kolmårdens djurpark (Ruby on Rails)",
        "Stadium Sports Camp (Ruby on Rails)",
        "Bibelstund (iOS/JavaScript/React/Titanium/Python)",
		"Secret project for Apple (HTML/CSS/JavaScript)",
		"ZooBooks by ZooWho (iOS/Objective-C/app marketing)"
      ],
    },
  ];
</script>

<Accordion>
  {#each jobs as job}
    <AccordionItem>
      <svelte:fragment slot="title">
        <h5>{job.name} {job.year}</h5>
        <div>{job.role}</div>
      </svelte:fragment>
      <p>
        {job.description}
      </p>
      {#if job.projects}
        <h6 class="mt-4">Projects:</h6>
        <UnorderedList>
          {#each job.projects as project}
            <ListItem>
              <p>{project}</p>
            </ListItem>
          {/each}
        </UnorderedList>
      {/if}
    </AccordionItem>
  {/each}
</Accordion>
