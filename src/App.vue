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
				<div>
					<span style="color: #B982B6;">guest</span>@<span style="color: #FFFF34;">portfolio</span>
				</div>
				<section>
					<button class="tab-button"
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

*
{
	font-family: Consolas,monaco,monospace;
}

h2
{
	text-align: center;
}

.terminal header
{
	display: flex;
	flex-direction: column;
	justify-content: start;
	align-items: center;
	justify-content: center;
	background-color: #2e2e2e;
	width: 100%;
	padding: 3px;
	border-bottom: 3px solid white;
	color: white;
}

.terminal header section
{
	display: flex;
	flex-direction: row;
	justify-content: center;
	align-items: center;
	gap: 10px;
	width: 100%;
	padding: 10px;
}

.tab-button
{
	background-color: #201F1F;
	width: 50%;
	padding: 6px;
	border: none;
	color: white;
}

.tab-button:hover
{
	background-color: #343434;
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
	border: 3px solid white;
}

body
{
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
	background-color: black;
	/* border: 1px solid red; */
	width: 100vw;
	height: 100vh;
}

</style>