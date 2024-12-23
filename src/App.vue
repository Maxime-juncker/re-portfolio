<script setup>
import tabA from './components/tabA.vue';
import tabB from './components/tabB.vue';

import { ref } from 'vue';

const current_tab = ref("tabA");

const tabs =
{
	tabA,
	tabB
}

</script>

<template>
	<body>
		<div id="terminal" class="terminal">
			<header>
				<h2 class="title">guest@portfolio</h2>
				<section>
					<!-- <button>Tab a</button>
					<button>Tab b</button>
					<button>Tab c</button> -->
					<button
					v-for="(_, tab) in tabs"
						:key="tab"
						:class="['tab-button', { active: current_tab === tab }]"
						@click="current_tab = tab"
					>
					{{ tab }}
				</button>
				</section>
			</header>
	  <component :is="tabs[current_tab]" class="tab"></component>
	   </div>
	</body>
</template>

<style scoped>

h2
{
	text-align: center;
}

.terminal header
{
	background-color: grey;
	width: 100%;
	border-bottom: 3px solid red;

}

.terminal header section
{
	display: flex;
	flex-direction: row;
	justify-content: center;
	align-items: center;
	background-color: green;
	gap: 10px;
	width: 100%;
	padding: 10px;
}
.terminal header section button
{
	width: 33%;
}

.terminal
{
	display: flex;
	flex-direction: column;
	justify-content: start;
	align-items: center;
	background-color: #1f1f1f;
	width: 70%;
	height: 100%;
	margin: 100px;
	border: 3px solid red;

}

body
{
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
	background-color: black;
	border: 1px solid red;
	width: 100vw;
	height: 100vh;
}

</style>