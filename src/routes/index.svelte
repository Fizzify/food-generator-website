<script context="module">
	export async function load({ fetch }) {
		const res = await fetch('https://www.themealdb.com/api/json/v1/1/random.php');
		const data = await res.json();
		if (res.ok) {
			return {
				props: { food: data.meals[0] }
			};
		}
	}
</script>

<script>
  import Foods from '../components/Foods.svelte';
  import NavBar from '../components/NavBar.svelte';
	export let food;
</script>

<body>
	<NavBar />
	<section class="home">
		<Foods {food} />
	</section>
</body>

<svelte:head>
	<style>
		@import url('https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,700;1,400&display=swap');

		body {
			background-color: #ffedb3;
		}

		.home {
			font-family: 'Playfair Display', serif;
			text-align: center;
		}

		.food-title {
			font-size: 3rem;
		}

		.food-img {
			border-radius: 5px;
			box-shadow: 0px 0px 20px rgba(0, 0, 0, 0.3);
		}

		.btn {
			padding: 1em;
		}

		.generate {
			background-color: #ff0000;
			padding: 0.5em 2em;
			color: white;
			text-decoration: none;
			border-radius: 10px;
			box-shadow: 0px 0px 50px rgba(0, 0, 0, 0.2);
			font-family: Arial, sans-serif;
			font-size: 1.5rem;
		}
	</style>
</svelte:head>
