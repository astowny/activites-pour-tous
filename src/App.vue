<template>
	<v-app>
		<!-- <v-app-bar app color="primary" dark></v-app-bar> -->
		<v-content>
			<v-container>
				<!-- header -->
				<v-row>
					<v-col align="center">
						<h1 class="h3">
							BESOIN DE MOTIVATION POUR ATTEINDRE VOS OBJECTIFS ?
							LES ACTIVITES PHYSIQUES POUR TOUS VOUS Y AIDERONT
						</h1>
						<div class="subtitle-1">Que vous soyez sportif, débutant ou non vous pouvez le faire !</div>
					</v-col>
				</v-row>
				<!-- activites -->
				<v-row v-for="(rowActivite,i) in textActivites" :key="`rowActivite${i}`" align="stretch" justify="space-around" class="ma-3">
					<v-card
						v-for="(text,j) in rowActivites"
						:key="`rowActivite${i}-activite${j}`"
						class="ma-3 pa-3 body-1 text-justify"
						max-width="200"
					>{{ text }}</v-card>
				</v-row>
				<div>
					PRENEZ VOTRE SANTE EN MAIN EN BENEFICIANT DES BIENTFAITS DE L’ACTIVITE PHYSIQUE ET EN DECOUVRANT VOS CAPACITES SPORTIVES.
					GYM D’ENTRETIEN POUR MAINTENIR VOTRE FORME ET VOTRE CONDITION PHYSIQUE BASEE SUR UN PROGRAMME PERSONNALISE ET ADAPTE.
					VOTRE COACH SPORTIF DIPLÔMEE D’ETAT SE DEPLACE CHEZ VOUS POUR VOUS PROPOSER DIFFERENTES PRESTATIONS DE SERVICES PERSONNALISEES SELON VOS OBJECTIFS.
				</div>
				<div>
					<p>COURS INDIVIDUEL OU EN GROUPE, EN INTERIEUR OU EN EXTERIEUR (EN FONCTION DE LA METEO ET DES CONTRAINTES SANITAIRES).</p>

					<p>
						TARIFS :
						<ul>
							<li></li>
						</ul>
						A PARTIR DE 6 PERSONNES : 5€/séance/personne.
						De 3 à 5 PERSONNES : 10€/séance/personne.
						COURS PARTICULIERS : 30€ /séance de 1H 270€ les 10 séances.
					</p>
					<p>
						N.B. : déduction fiscale 50%, au titre des prestations de services
						Contactez Thi Chap (Katy)
						<br />Educatrice Sportive diplômée d’état fitness et APT (Activités Physiques pour Tous)
						<br />06 52 59 18 49
						<br />thichaptran@gmail.com
					</p>
				</div>
			</v-container>
		</v-content>
	</v-app>
</template>

<script>
export default {
	name: "App",

	components: {},

	data: () => ({
		//
		textActivites: [
			[
			"Echauffement, mobilisation des articulations inspirés du taïchi, qi gong, pilates et yoga",
			"Renforcement musculaire progressif avec ou sans matériel (cuisses-abdo-fessiers, gainage)",
			"Travail d’équilibre, de coordination et de mémoire"
			],
			[ 
				"Cardio adaptée en fonction de votre niveau",
			"Etirement, souplesse, respiration, détente, relaxation, méditation, libération de stress et bien être"
			]
		]
	})
};
</script>
