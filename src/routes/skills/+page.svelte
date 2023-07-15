<script lang="ts">
	import {
		StructuredList,
		StructuredListHead,
		StructuredListRow,
		StructuredListCell,
		StructuredListBody
	} from 'carbon-components-svelte';

	let skills = [
		{ skill: 'Accessability', level: '3/5', about: 'Description' },
		{ skill: '3D computer graphics', level: '3/5', about: 'Description' },
		{ skill: 'More to be added...', level: 'Various', about: 'See projects for now' }
	];
</script>

<StructuredList>
	<StructuredListHead>
		<StructuredListRow head>
			<StructuredListCell head>Skill</StructuredListCell>
			<StructuredListCell head>Level</StructuredListCell>
			<StructuredListCell head>About</StructuredListCell>
		</StructuredListRow>
	</StructuredListHead>
	<StructuredListBody>
		{#each skills as { skill, level, about }}
			<StructuredListRow>
				<StructuredListCell noWrap>{skill}</StructuredListCell>
				<StructuredListCell>{level}</StructuredListCell>
				<StructuredListCell>
					{about}
				</StructuredListCell>
			</StructuredListRow>
		{/each}
	</StructuredListBody>
</StructuredList>
