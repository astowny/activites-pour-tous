<template>
	<v-app>
		<v-content>
			<!-- banner header -->
			<v-card width="100%" height="400" elevation="0" tile class="overflow-hidden">
				<Banner />
			</v-card>
			<v-container>
				<!-- activites -->
				<v-row align="stretch" justify="space-around">
					<v-col v-for="(card,i) in cardsActivities" :key="'card' + i" :cols="card.flex">
						<v-sheet :color="card.color" height="100%">
							<v-card-text>{{ card.text }}</v-card-text>
						</v-sheet>
					</v-col>
				</v-row>
				<v-row>
					<v-col v-for="(item, i) in paragraphs" :key="'paragraph' + i" cols="12" md="3">
						<p class="text-center">
							<v-img class="mx-auto" width="50" :src="item.src" :alt="item.alt"></v-img>
							{{ item.text }}
						</p>
					</v-col>
				</v-row>
				<v-row align="stretch" justify="space-around">
					<v-card
						v-for="(cardPrice, i) in cardsPrices"
						:key="i + '-' + cardPrice.title"
						class="text-center white--text ma-2 pt-2 pb-5 px-4"
						elevation="5"
						min-width="310"
						color="red"
					>
						<div class="text-h3 text-center">{{ cardPrice.title }}</div>
						<p>{{ cardPrice.nbPeople }}</p>
						<div class="font-weight-bold text-display1">{{ cardPrice.price }}</div>
						<div>{{ cardPrice.unit }}</div>
						<div
							v-if="cardPrice.discount"
							class="font-italic text-h3 red--text text--lighten-4"
						>{{ cardPrice.discount }}</div>
					</v-card>
				</v-row>
				<p class="text-center font-italic">{{ notaBene }}</p>

				<!-- contact -->
				<div>
					<h2>{{ contactInfos.nameTitle }}</h2>
					<p>
						{{ contactInfos.diploma }}
						<br />
						<strong class="red--text text--darken-2">{{ contactInfos.phone }}</strong>
						<br />
						<strong class="red--text text--darken-2">{{ contactInfos.mail }}</strong>
					</p>
				</div>
			</v-container>
		</v-content>
	</v-app>
</template>
<script>
import Banner from "./components/Banner/index";
export default {
	name: "App",

	components: {
		Banner
	},

	data: () => ({
		//
		cardsActivities: [
			{
				color: "red lighten-1",
				text:
					"Echauffement, mobilisation des articulations inspirés du taïchi, qi gong, pilates et yoga",
				flex: 6
			},
			{
				color: "red lighten-3",
				text:
					"Renforcement musculaire progressif avec ou sans matériel (cuisses-abdo-fessiers, gainage)",
				flex: 6
			},
			{
				color: "red lighten-3",
				text: "Travail d’équilibre, de coordination et de mémoire",
				flex: 6
			},
			{
				color: "red lighten-1",
				text: "Cardio adaptée en fonction de votre niveau",
				flex: 6
			},
			{
				color: "red lighten-1",
				text:
					"Etirement, souplesse, respiration, détente, relaxation, méditation, libération de stress et bien être",
				flex: 12
			}
		],
		paragraphs: [
			{
				src: "https://img.icons8.com/ios/50/000000/heart-with-pulse.png",
				text:
					"PRENEZ VOTRE SANTE EN MAIN EN BENEFICIANT DES BIENTFAITS DE L’ACTIVITE PHYSIQUE ET EN DECOUVRANT VOS CAPACITES SPORTIVES."
			},
			{
				src: "https://img.icons8.com/ios/50/000000/pushups.png",
				text:
					"GYM D’ENTRETIEN POUR MAINTENIR VOTRE FORME ET VOTRE CONDITION PHYSIQUE BASEE SUR UN PROGRAMME PERSONNALISE ET ADAPTE."
			},
			{
				src: "https://img.icons8.com/ios/50/000000/home-page.png",
				text:
					"VOTRE COACH SPORTIF DIPLÔMEE D’ETAT SE DEPLACE CHEZ VOUS POUR VOUS PROPOSER DIFFERENTES PRESTATIONS DE SERVICES PERSONNALISEES SELON VOS OBJECTIFS."
			},
			{
				src: "https://img.icons8.com/ios/50/000000/groups.png",
				text:
					"COURS INDIVIDUEL OU EN GROUPE, EN INTERIEUR OU EN EXTERIEUR (EN FONCTION DE LA METEO ET DES CONTRAINTES SANITAIRES)."
			}
		],
		attributionsLinks: [
			`<a href="https://icons8.com/icon/7665/pompes">Pompes icon by Icons8</a>`,
			`<a href="https://icons8.com/icon/35583/coeur-avec-pouls">Coeur avec pouls icon by Icons8</a>`,
			`<a href="https://icons8.com/icon/53382/page-d’accueil">Page d’accueil icon by Icons8</a>`,
			`<a href="https://icons8.com/icon/3734/groupe-d'utilisateurs">Groupe d'utilisateurs icon by Icons8</a>`
		],
		cardsPrices: [
			{
				title: "Gros groupe",
				nbPeople: "À partir de 6 personnes",
				price: "5€",
				unit: "/séance/personne"
			},
			{
				title: "Petit groupe",
				nbPeople: "De 3 à 5 personnes",
				price: "10€",
				unit: "/séance/personne"
			},
			{
				title: "Cours particuliers",
				nbPeople: "De 1 à 2 personnes",
				price: "30€",
				unit: "/séance de 1h",
				discount: "270€ les 10 séances"
			}
		],
		notaBene:
			"N.B. : déduction fiscale 50%, au titre des prestations de services",
		contactInfos: {
			nameTitle: "Contactez Tchi Chap (Katy)",
			diploma:
				"Educatrice Sportive diplômée d'état fitness et APT (Activités Physiques pour Tous)",
			phone: "06 52 59 18 49",
			mail: "thichaptran@gmail.com"
		}
	})
};
</script>
<style>
.overflow-hidden {
	overflow: hidden;
}
.text-h3 {
	font-size: 30px;
}
.text-display1 {
	font-size: 50px;
	line-height: 50px;
}
</style>