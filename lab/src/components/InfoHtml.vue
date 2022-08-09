<template>
  <div id="info">
	<h1>Some sum:</h1>
	<h2>My age will be {{29 + 1}} by the end of the month</h2><br>

	<h1>Some good lema:</h1>
	<h2>Siempre papi, {{ printPapi() }}</h2><br>

	<h1>Some Simpsons phrase in castellano de España porque es el mejor:</h1>
	<h2 v-show="showSimpsonsPhrase">No conquistas nada, con una ensalada</h2><br>

	<h1>Some drippin' mangas:</h1>
	<h2 v-for="manga in mangasCanela" :key="manga">
		{{manga.name}} was created by {{manga.author}} and first published in {{manga.date}}.
	</h2><br>

	<h1>Some bonus:</h1>
	<div  v-show="niceMeme" class="background"></div>
	<button @click="niceMeme = true">Click me to see what my teachers will think when seeing this cool lab</button>
  </div>
</template>

<script>
export default {
	name: "InfoHtml",
	data() {
		return{
			showSimpsonsPhrase: true,
			mangasCanela:[
			{
				name: "Samurai Shamploo",
				author: "Sinichito Watanabe",
				date: 2004
			},
			{
				name: "Dororo",
				author: "Osamu Tezuka",
				date: 1967
			},
			{
				name: "Attack on titan",
				author: "Hajime Isayama",
				date: 2009
			}
			],
			niceMeme: false,
			memeClass: "background",
		}
	},
	methods:{
		printPapi(){
			return "nunca inpapi";
		}
	},

}
</script>

<style>

h1{
	font-family: 'roboto';
}
h2{
	font-family: 'roboto';
	color: lightcoral;
}

.background {
	background-image: url(https://www.kidscodecs.com/wp-content/uploads/2020/02/History_TS_ProgrammingMemes_image4.png);
	background-repeat: no-repeat;
	background-size: cover;
	background-position: center;
	width: 600px;
	height: 500px;
}
</style>