<script setup>
defineProps({
		Str1: String,
		Str2: String,
		Str3: String,
		Str4: String,
		Str5: String,
		Link_class: String
	})
</script>

<template>
	<section class="list-elt">
		<p style="color: #FF5E5E;">{{ Str1 }}</p>
		<p style="color: #5EFF68;">{{ Str2 }}</p>
		<p style="color: #53C3F3;">{{ Str3 }}</p>
		<p style="color: #5EFF68;">{{ Str4 }}</p>
		<a style="color: #B982B6;" :class="Link_class" :href="Str5" target="_blank" rel="noopener noreferrer">{{ Str5 }}</a>
	</section>
</template>

<style scoped>
	.list-elt
	{
		width: 100%;
		display: grid;
		grid-template-columns: 15% 20% 15% 10% 40%;
		margin: 0;
		padding: 0;
	}

	.list-elt p
	{
		color: white;
		margin: 0;
		word-spacing: 0px;
		padding: 0;
	}

	a
	{
		color: white;
	}

	a:hover
	{
		background-color: transparent;
		color: white;
	}

	.link:hover
	{
		text-decoration: underline;
	}

	@media (max-width: 1000px)
	{
		.list-elt
		{
			grid-template-columns: 30% 40% 30% 20% 80%;
			gap: 15%;
		}
	}
</style>