<script lang="ts">
	import Project from "../../components/project.svelte";
</script>

<div class="grid grid-cols-1 w-full">
	<Project
		name="SumoBot Wars"
		items={['LiU Game Awards, 2nd place']}
		link="https://www.youtube.com/embed/Ls2c9tOACmU"
	>
		Unreal Engine, dynamic AI enemy behaviour, Blueprints, local multiplayer, player testing, game
		design
	</Project>

	<Project link="https://www.youtube.com/embed/pTzU9L-jnaE" name="Rainbone"
		>GLSL, C++, dome, voice controlled, collaborative, game design, accessability
	</Project>

	<Project
		items={['Best interaction design, C Awards']}
		link="https://www.youtube.com/embed/fcklnezF1vg"
		name="Ladybug"
		>Java, Android, multiplayer
	</Project>
	<Project link="https://www.youtube.com/embed/XTrzX8AoE-w" name="7 Light-years"
		>Unity, level design</Project
	>
</div>
