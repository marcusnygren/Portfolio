<script lang="ts">
  import { ListItem, UnorderedList } from "carbon-components-svelte";
  import Project from "../../../components/project.svelte";
</script>

<div class="grid grid-cols-1 w-full">
  <h3 class="mb-8 uppercase">Professionally</h3>

  <Project
    year="2022-2023"
    name="Citizen portal"
    client="Norconsult Digital / Bergen kommune"
    functionalities={[
      "Forms",
      "My pages",
      "Map functionality",
      "UX/UI design",
      "Building UI components",
      "Custom design system",
      "Automatic tests",
      "Accessability (WCAG 2.1 AA compliance)",
      "User research/testing",
    ]}
    tools={[
      "Svelte",
      "yup",
      "TypeScript",
      "Vite",
      "Playwright",
      "Storybook",
      "testing-library",
      "msw",
      "OpenLayers",
      "Figma",
      "Tailwind",
    ]}
    links={[
      "https://www.bergenskart.no/portal/apps/sites/#/bergenskart/apps/504ddef40b8e425cb0e7fe4903d76140/explore",
    ]}
    iframe=""
    >Customer portal for applying and managing parking permits via using a map,
    built from the ground-up in Svelte/TypeScript.
  </Project>

  <Project
    name="Web GIS application (NDA)"
    client="Telia"
    functionalities={[
      "Map interaction",
      "New functionality",
      "Forms",
      "Bug fixes",
      "User research",
      "System design",
      "Automatic tests",
      "Co-design workshops",
      "UX/UI design",
    ]}
    iframe="https://openlayers.org/en/latest/examples/mobile-full-screen.html"
    year="2021-2022"
    tools={[
      "React",
      "React Hook Form",
      "OpenLayers",
      "Redux",
      "D3.js",
      "Material UI",
      "UX/service design",
    ]}
    >Since I can't show it, to the right you can see an example of a responsive
    map in OpenLayers.</Project
  >
  <Project
    name="Skriv under"
    client="Fridays for Future"
    year="2019"
    functionalities={["Frontend", "Responsiveness"]}
    iframe="https://skrivunder.fridaysforfuture.se/"
    links={["https://skrivunder.fridaysforfuture.se/"]}
    tools={["React", "Gatsby", "JavaScript", "Amazon Web Services", "Vercel"]}
  />
  <Project
    name="Early DynaMaker concept & UX design"
    client="SkyMaker"
    year="2018"
    functionalities={[
      "Design for learning",
      "UX design",
      "Teaching",
      "Coaching",
      "Concept",
    ]}
    link="d66_10JTntM"
    links={["https://docs.dynamaker.com/good-to-know"]}
    >Consultant for SkyMaker, in preperation for them wanting to create a
    UI/code tool where customers themselves could create 3D web configurators.
  </Project>
  <Project
    name="Bibelstund"
    links={[
      "https://www.bibelnidag.org/bibelstund/",
      "https://apps.apple.com/se/app/bibelstund/id1015327402",
    ]}
    functionalities={["Frontend", "Backend"]}
    client="Swedish Bible Society"
    year="2014"
    tools={[
      "React",
      "Reflux",
      "Python",
      "Django",
      "HTML",
      "CSS",
      "Cordova",
      "Titanium",
    ]}
    link="kEFQtzDrtnk"
  />

  <h3 class="mb-8 mt-8 uppercase">Internal</h3>
  <Project
    year="2023"
    name="marcusnygren.se"
    iframe="https://marcusnygren.se"
    tools={["SvelteKit", "TypeScript", "Tailwind", "Carbon Design System"]}
  />

  <!--
  <Project
    year="2011-2015"
    name="marcusnygren.se (WordPress)"
    iframe="https://web.archive.org/web/20140109165842/http://www.marcusnygren.se/"
  />
  <Project
    year="2016"
    name="marcusnygren.se"
    iframe="https://web.archive.org/web/20180417110339/http://marcusnygren.se/"
  >(via Wayback Machine)</Project>-->

  <Project
    name="Kodkartan"
    year="2017-2018"
    client="Edvira"
    iframe="https://web.archive.org/web/20180321010112/https://kodkartan.se/"
    tools={["React", "maps", "Meteor", "Node", "Express", "MongoDB", "Heroku"]}
    >A map which visualizes Swedish municipalities' introduction of programming
    in schools (running in Wayback Machine, so unfortunately the map/API data
    won't be loaded).</Project
  >

  <h3 class="mb-8 mt-8 uppercase">University projects</h3>

  <Project
    name="YoungDrive App"
    client="YoungDrive / Plan International"
    link="wydaHRkNAGo"
    year="2016"
    links={[
      "uganda.pdf",
      "https://www.researchgate.net/publication/335840966_Developing_a_Mobile_Learning_Application_for_Entrepreneurship_Education_in_Uganda_and_Zambia",
      "https://www.linkedin.com/pulse/developing-mobile-learning-application-education-uganda-marcus-nygren/",
    ]}
    tools={[
      "React",
      "JavaScript",
      "HTML",
      "CSS",
      "Node",
      "Meteor",
      "Cordova",
      "mongoDB",
      "Heroku",
      "GitHub",
      "CI/CD",
      "iOS",
      "Android",
      "web",
    ]}
  />

  <Project
    name="IKEAswipe"
    client="Combitech"
    year="2015"
    link="aMqjUe7OPVU"
    tools={["Android", "Java", "Metalo SDK", "AR"]}
  >
    <p class="mb-4">
      Android application using the Metaio SDK for augmented reality. Open
      Source on <a href="https://github.com/antonosterblad/IKEAswipe">GitHub</a>
    </p>

    <p class="mb-2">
      IKEAswipe is a digital assembly instruction using augmented reality. The
      project was developed in the course TNM082, Agile usability development
      for handheld devices, at Linköping University.
    </p>

    <p>
      Note that this project is no cooperation with IKEA and the we own no
      rights to their copyright protected material. The project is a beta
      version and we do not intend to launch it.
    </p>
  </Project>

  <Project
    name="Inhibitor"
    year="2012"
    iframe="/inhibitor.pdf"
    links={[
      "inhibitor.pdf",
      "https://web.archive.org/web/20130601051847/http://3d.marcusnygren.se/",
    ]}
    tools={[
      "WebGL",
      "JavaScript",
      "HTML",
      "CSS",
      "jQuery",
      "ThreeJS",
      "3DS Max",
    ]}
  />

  <h3 class="mb-8 mt-8 uppercase">Hackathons</h3>
  <Project
    name="Traviz"
    tools={[
      "WebGL",
      "JavaScript",
      "HTML",
      "CSS",
      "linear algebra",
      "jQuery",
      "Google Maps",
    ]}
    client="East Sweden Hack"
    year="2012"
    link=""
    vimeo
    >Traffic accident visualizer using open data, WebGL and Google Maps. Demo
    starts at 1:30.</Project
  >
</div>
