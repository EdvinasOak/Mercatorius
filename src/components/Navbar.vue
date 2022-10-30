<template>
	<NavBar>
		<ul class="nav-list">
			<li role="button">
				<router-link class="nav-link" to="/">Home</router-link>
			</li>
			<li>
				<router-link class="nav-link" to="/services">Services</router-link>
			</li>
			<li>
				<router-link class="nav-link" to="/about">About</router-link>
			</li>
		</ul>
	</NavBar>
</template>

<script lang="ts">
	export default {
		name: 'NavBar',
		props: {
			title: String,
			showAddTask: Boolean,
		},
		components: {},
	};
</script>

<style scoped>
	NavBar {
		width: 15vh;
		background: transparent;
		position: fixed;
		bottom: 10%;
		right: 0;
		height: 10% !important;
	}
	.nav-list {
		list-style: none;
		margin: 0;
		/* padding: 0px 0px 0px 41px; */
		text-align: left;
		letter-spacing: -0.04em;
		font-family: Verdana, Geneva, Tahoma, sans-serif;
		font-weight: bold;
		padding-right: 10%;
	}

	li {
		font-size: 1.2em;
		margin: 10px 0;
		line-height: 0.8em;
	}

	.nav-link {
		text-decoration: none;
		color: #fffffe;
	}

	.nav-link:hover {
		cursor: pointer;
		color: #fdefb2;
		font-size: 1.6em;
		transition: 0.1s;
		/* border-left: 2px solid #fdefb2; */
		/* box-shadow: inset 100px 0 0 0 #fdefb2; */
	}

	@media (max-width: 899px) {
		NavBar {
			width: 100%;
			background: transparent;
			/* position: fixed; */
			bottom: 0;
			right: 0;
			height: 4% !important;
			margin: 0 -5vw 0 0;
		}

		.nav-list {
			list-style: none;
			font-family: Verdana, Geneva, Tahoma, sans-serif;
			font-weight: bold;
			display: inline-block;
		}
		li {
			float: left;
			/* padding: 1vw; */
			/* text-align: center; */
			/* padding-right: 1vw; */
			font-size: 1rem;
		}
		li a {
			text-decoration: none;
			padding: 3vw;
		}
	}
</style>
