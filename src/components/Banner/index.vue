<template>
	<v-row justify="center">
		<v-col cols="12" class="pa-0">
			<v-row align="center">
				<!-- in overlay -->
				<v-overlay :absolute="absolute" :opacity="opacity" :value="overlay" :z-index="zIndex">
					<div class="text-center">
						<h1>BESOIN DE MOTIVATION POUR ATTEINDRE VOS OBJECTIFS ?</h1>
						<div class="text-h1">LES ACTIVITES PHYSIQUES POUR TOUS VOUS Y AIDERONT</div>
					</div>
				</v-overlay>
			</v-row>
		</v-col>

		<!-- under overlay -->
		<v-row justify="center">
			<v-img class="visible-xs" src="./fitness-banner-mobile.jpg" alt="Fitness"></v-img>
			<v-img class="hidden-xs" src="./fitness-banner.jpg" alt="Fitness" max-height="400"></v-img>
		</v-row>
	</v-row>
</template>

<script>
export default {
	data: () => ({
		absolute: true,
		opacity: 0.46,
		overlay: true,
		zIndex: 5,
		srcImg: "./banner.png"
	})
};
</script>

<style>
</style>