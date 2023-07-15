<script>
	import {
		Header,
		HeaderNav,
		HeaderNavItem,
		HeaderNavMenu,
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
		Column
	} from 'carbon-components-svelte';
	import { LogoLinkedin } from 'carbon-icons-svelte';

	let isSideNavOpen = false;
</script>

<Header company="Developer" platformName="Marcus Nygren" bind:isSideNavOpen>
	<svelte:fragment slot="skip-to-content">
		<SkipToContent />
	</svelte:fragment>
</Header>

<SideNav bind:isOpen={isSideNavOpen}>
	<SideNavItems>
        <SideNavMenuItem href="/" text="About" />
		<SideNavLink href="career" text="Career" />
		<SideNavMenu text="Projects">
			<SideNavMenuItem href="games" text="Games" />
			<SideNavMenuItem href="web" text="Web" />
		</SideNavMenu>
		<SideNavLink href="skills" text="Skills" />
		<SideNavDivider />
		<SideNavLink href="https://www.linkedin.com/in/marcusnygren/en-US" text="LinkedIn" />
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
