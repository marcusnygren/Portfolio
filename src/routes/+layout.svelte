<script lang="ts">
  import "../app.css";
  import "carbon-components-svelte/css/g100.css";
  import {
    Header,
    SideNav,
    SideNavItems,
    SideNavMenu,
    SideNavMenuItem,
    SideNavLink,
    SideNavDivider,
    SkipToContent,
    Content,
    Grid,
    Row,
    Column,
  } from "carbon-components-svelte";

  let isSideNavOpen = true;
</script>

<Header company="Developer" platformName="Marcus Nygren" bind:isSideNavOpen>
  <svelte:fragment slot="skip-to-content">
    <SkipToContent />
  </svelte:fragment>
</Header>

<SideNav bind:isOpen={isSideNavOpen} rail>
  <SideNavItems>
    <SideNavMenuItem href="/" text="About" />
    <SideNavLink href="/career" text="Career" />
    <SideNavMenu text="Projects">
      <SideNavMenuItem href="/projects/games" text="Games" />
      <SideNavMenuItem href="/projects/web" text="Web" />
    </SideNavMenu>
    <SideNavLink href="/teaching" text="Teaching" />
    <!--<SideNavLink href="/skills" text="Skills" />
    <SideNavLink href="/research" text="Research" />-->
    <SideNavDivider />
    <SideNavLink
      href="https://www.linkedin.com/in/marcusnygren/en-US"
      text="LinkedIn"
    />
  </SideNavItems>
</SideNav>

<Content>
  <Grid>
    <Row>
      <Column>
        <slot />
      </Column>
    </Row>
  </Grid>
</Content>
