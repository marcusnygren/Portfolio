<script lang="ts">
  import Project from "../../../components/project.svelte";

  /*const projects = [
    {
      name: "IKEAswipe",
      link: "aMqjUe7OPVU",
      items: ["Android, Java, Metalo SDK, AR"],
      year: "",
    },
  ];*/
</script>

<div class="grid grid-cols-1 w-full">
  <h3 class="mb-8 uppercase">Professionally</h3>
  <Project
    name="PlayIt"
    client="Uppsala University, Linköpings kommun, Ecorado, KTH, Drakryggen"
    year={"2018 (-2021)"}
    functionalities={[
      "Concept",
      "Technical feasability",
      "Raspberry Pi programming",
      "UI design",
      "Network communication",
      "User testing",
      "Game design",
      "Block/flow-based programming",
    ]}
    tools={[
      "C",
      "Arduino",
      "Raspberry Pi",
      "Python",
      "Node",
      "JavaScript",
      "Blockly",
      "Unity",
      "Azure",
    ]}
    link="0ud-mT21imw"
    links={[
      "https://www.youtube.com/watch?v=Lioc2Ulksco",
      "https://www.playnetwork.se/playit/",
      "https://www.im.uu.se/forskning/projekt/play-it/",
      "https://api.iotsverige.se/wp-content/uploads/2022/03/Play-IT-Slutrapport-till-IoT-Sverige.pdf",
      "https://linkopingsciencepark.se/en-lekplats-dar-leken-aldrig-tar-slut/",
      "https://linkopingsciencepark.se/lekfullt-iot-play-it/" /*Teknisk demo*/,
      "https://play.linkoping.se/media/ukEjtRtn9IyrISQMBSPInQ/magistratshagen-de-lekfulla-sakernas-internet" /*Video*/,
      "https://odysee.com/@JonBck:e/how-to-see-play-play-traces:3",
      "https://www.diva-portal.org/smash/get/diva2:1575065/FULLTEXT01.pdf" /*Exjobb*/,
    ]}
  >
    Vinnova innovation project. Inspired by Scratch Jr, Blockly and Internet of
    Things, we built a playground that kids themselves could remake via
    graphical programming. It needed to be accessible, durable, fun, and
    intuitive. I was a consultant to the researchers; doing feasability
    evaluations, doing the first prototype, breaking down concepts and user
    stories into technical and UX tasks, and technical hand-over after the first
    prototype was successful.
  </Project>
  <h3 class="mb-8 mt-8 uppercase">Game jams</h3>
  <Project
    year={"2022"}
    name="Monster math"
    image="monster-math.png"
    links={["https://saperoo.itch.io/monstermath"]}
    ><p>Unity, level design</p>
    <p>
      Project for the global GMTK Game Jam 2022, themed "Roll of the Dice".
      "That theme might immediately spark ideas of randomness and probability,
      or board games and casinos, but as always - you can interpret this theme
      however you like."
    </p></Project
  >
  <Project
    year="2015"
    functionalities={["Game design", "Game programming"]}
    tools={["Unity"]}
    name="Express Delivery"
    image="express-delivery.png"
    links={[
      "https://henrikelode.com/express-delivery/",
      "https://tomekpaszek.itch.io/express-delivery",
    ]}
  >
    For Nordic Game Jam 2015 in Copenhagen. Tags: arcade, maternity simulator,
    taxi driving, babies. Review:
    https://www.alphabetagamer.com/express-delivery-game-jam-build/
  </Project>
  <Project
    link="XTrzX8AoE-w"
    year={"2013"}
    name="7 Light-years"
    tools={["Unity"]}
    links={["https://nifflas.ni2.se/miscgames/"]}
    functionalities={["Level design", "Art"]}
  >
    <p>
      My first project in Unity, together with my amazin cousin Nifflas on
      Christmas Day.
    </p></Project
  >
  <h3 class="mb-8 mt-8 uppercase">Awards (university projects)</h3>
  <Project
    link="pTzU9L-jnaE"
    items={["1st place in Next public magnet, C Awards"]}
    name="Rainbone"
    year="2016"
    tools={[
      "GLSL",
      "C++",
      "dome",
      "voice controlled",
      "collaborative",
      "game design",
      "accessability",
    ]}
  >
    <p>
      A voice controlled cooperative game. It was developed mainly for dome
      theaters (up to 100 players), but it is also portable to 2D screens and
      Oculus Rift. Open source on Github.
    </p>
  </Project>
  <Project
    name="SumoBot Wars"
    year="2015"
    items={["2nd place in Best game, LiU Game Awards"]}
    link="Ls2c9tOACmU"
    tools={[
      "Unreal Engine 4 (Blueprints)",
      "dynamic AI enemy behaviour",
      "local multiplayer",
      "player testing",
      "game design",
      "photography/video editing",
    ]}
  />

  <Project
    items={["1st place in Best interaction design, C Awards"]}
    link="fcklnezF1vg"
    name="Ladybug"
    year="2014"
    tools={["Java", "Android", "multiplayer", "MATLAB", "Box2D"]}
  />
</div>
