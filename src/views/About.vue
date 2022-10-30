<template>
	<div class="about">
		<div class="hero_text hero_text--list">
			<div class="hero_text_container">
				<div class="text_container">
					<li class="mercatorius">About</li>
					<li class="one_market">One market</li>
					<li class="one_app">One app</li>
				</div>
			</div>
			<div class="logo"></div>
		</div>
		<Navbar />
	</div>
</template>

<script>
	import { defineComponent } from 'vue';
	import Navbar from '../components/Navbar.vue';

	export default defineComponent({
		name: 'About',
		components: {
			Navbar,
		},
	});
</script>

<style lang="scss" scoped>
	.about {
		background: #0f0e17;
		overflow: hidden;
		height: 100vh;
	}

	.home {
		background: #0f0e17;
		overflow: hidden;
		height: 100vh;
	}
	@media (max-width: 899px) {
		.hero_text {
			grid-template-columns: repeat(1, 30%, 70%);
			height: 30%;
			text-align: center;
			margin-top: 5%;
		}

		.one_market {
			padding-left: 0;
			line-height: 120%;
			font-size: 12vmin;
			color: #fffffe;
		}

		.one_app {
			padding-right: 0;
			line-height: 120%;
			font-size: 13vmin;
		}

		.mercatorius {
			line-height: 120%;
			padding-right: 0;
			font-size: 14vmin;
		}
	}

	@media (min-width: 900px) {
		.hero_text {
			grid-template-columns: repeat(2, 60%);
			height: inherit;
			font-size: 6vw;
		}

		.text_container {
			position: relative;
			top: 50vh;
			margin-right: 0.4em;
		}

		.one_market {
			padding-left: 30%;
			line-height: 7vh;
		}

		.one_app {
			padding-right: 35%;
			line-height: 7vh;
		}

		.mercatorius {
			// padding-right: 5%;
			padding-left: 5%;
			font-size: 7vw;
			line-height: 14llvh;
		}
	}

	.hero_text {
		display: grid;
		font-weight: bold;
		width: 100%;
		letter-spacing: -0.04em;
		font-family: Verdana, Geneva, Tahoma, sans-serif;
		/* font-size: calc((100vw - 376px) / 826 * 110 + 70px); */
		/* left: 5.3125vw; */
		&--list {
			list-style: none;
		}
	}

	.one_market {
		color: #fffffe;
	}

	.one_app {
		color: #fffffe;
	}

	.mercatorius {
		background-color: #004643;

		/* Gradient. */
		background-image: linear-gradient(45deg, #e53170, #ff8906);

		background-size: 100%;
		background-repeat: repeat;

		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
		-moz-background-clip: text;
		-moz-text-fill-color: transparent;
	}
</style>
