<script lang="ts">
  import Project from "../../components/project.svelte";

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
  <Project
    year={"2022"}
    name="Monster math (24h competition)"
    links={["https://saperoo.itch.io/monstermath"]}
    ><p>Unity, level design</p>
    <p>Solo (apart from the dice and the idea)</p>
    <p>
      Project for GMTK Game Jam 2022, themed "Roll of the Dice" ("That theme
      might immediately spark ideas of randomness and probability, or board
      games and casinos, but as always - you can interpret this theme however
      you like.")
    </p></Project
  >
  <Project
    name="PlayIt (consultant)"
    year={"2018-2021"}
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
    Internet of Things, Raspberry Pi, User research, playtesting, accessability,
    durability, play, game design, service design, Azure, Node, Blockly,
    Scratch.

    <p>Kids can re-program the installations</p>
  </Project>
  <Project link="pTzU9L-jnaE" name="Rainbone" year="2016"
    ><p>
      GLSL, C++, dome, voice controlled, collaborative, game design,
      accessability
    </p>
    <p>
      A voice controlled co-op game. It was developed mainly for dome theaters,
      but it is also portable to 2D screens and Oculus Rift. Open source on
      Github.
    </p>
  </Project>
  <Project
    name="SumoBot Wars"
    year="2015"
    items={["LiU Game Awards, 2nd place"]}
    link="Ls2c9tOACmU"
  >
    Unreal Engine, dynamic AI enemy behaviour, Blueprints, local multiplayer,
    player testing, game design
  </Project>

  <Project
    items={["Best interaction design, C Awards"]}
    link="fcklnezF1vg"
    name="Ladybug"
    year="2014"
    >Java, Android, multiplayer, MATLAB, Box2D

    <li>Report</li>
    <li>Trello board</li>
  </Project>
  <Project link="XTrzX8AoE-w" year={"2013"} name="7 Light-years (hobby)"
    ><p>Unity, level design</p>
    <p>My first project in Unity</p></Project
  >
</div>
