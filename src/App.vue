<script setup>
import resume from './components/resume_tab.vue';
import project from './components/project_tab.vue';
import contact from './components/contact_tab.vue';
import { ref } from 'vue';

const current_tab = ref("resume");

const tabs =
{
	resume,
	project,
	contact
}

</script>

<template>
	<body>
		<div id="terminal" class="terminal">
			<header class="term-header">
				<div>
					<span style="color: #DC6E47;">guest</span>@<span style="color: #FFFF34;">portfolio</span>
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
			<div class="tab-container">
				<component :is="tabs[current_tab]" class="tab"></component>
			</div>
	   </div>
	</body>
</template>

<style>

*
{
	font-family: Consolas,monaco,monospace;
}

h2
{
	text-align: center;
}

.term-header
{
	display: flex;
	flex-direction: column;
	justify-content: start;
	align-items: center;
	justify-content: center;
	background-color: #202020ab;
	width: 100%;
	padding: 3px;
	border-bottom: 3px solid white;
	color: white;
}

.term-header section
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
	width: 33%;
	padding-inline: 6px;
	padding-block: 9px;
	border: none;
	color: white;
	font-size: 18px;
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
	background-color: #00000071;
	backdrop-filter: blur(10px);
	width: 70%;
	height: 100%;
	border: 3px solid white;
	max-height: 100%;
}

.tab-container
{
	overflow-y: scroll;
	width: 100%;
	max-height: 100%;
}

body
{
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
	background-image: url("src/assets/screens.png");
	background-position: center;
	background-repeat: no-repeat;
	width: 100vw;
	height: 100vh;
	padding-block: 2%;

}

.tab
{
	padding: 1.5%;
	font-size: small;
	width: 100%;
	display: flex;
	flex-direction: column;
	justify-content: left;
	align-items: start;
	color: white;
}

.cursor
{
	animation: blinking 1.5s linear infinite;
}

@keyframes blinking
{
	0%, 50%
	{
		opacity: 100%;
	}
	51%, 100%
	{
		opacity: 0%;
	}
}


</style>