<script setup>
	import lstElt42 from './lst-elt-42.vue';

</script>

<template>
	<div class="tab">
		<div>
			<span>~/</span>
			<span style="color: #B982B6;">mjuncker</span>
			<span>/</span>
			<span style="color: #53C3F3;">home</span>/>
			<span>cat infos.txt</span>
		</div>
		<span>Pour plus d'infos sur les projets, clicker sur le liens github.</span>
		<p><br></p>
		<div>
			<span>~/</span>
			<span style="color: #B982B6;">mjuncker</span>
			<span>/</span>
			<span style="color: #53C3F3;">home</span>/>
			<span>cd 42_projects && ls</span>
		</div>
		<div>
			<span>~/</span>
			<span style="color: #B982B6;">mjuncker</span>
			<span>/</span>
			<span style="color: #53C3F3;">home</span>
			<span>/</span>
			<span style="color: #FFFF34;">42_projects</span>/>
		</div>
		<p><br></p>
		<lstElt42 -str1="name" -str2="status" -str3="last_updated" -str4="grade" -str5="link"/>
		<lstElt42 -str1="----" -str2="----" -str3="----" -str4="----" -str5="----"/>

		<lstElt42
		-str1="libft" -str2="validé" -str3="15 Nov 2024" -str4="125/100"
		-str5="https://github.com/Maxime-juncker/libft" -link_class="link"/>
		<lstElt42
		-str1="get_next_line" -str2="validé" -str3="20 Nov 2024" -str4="100/100"
		-str5="https://github.com/Maxime-juncker/get_next_line" -link_class="link"/>
		<lstElt42
		-str1="ft_printf" -str2="validé" -str3="23 Nov 2024" -str4="100/100"
		-str5="https://github.com/Maxime-juncker/ft_printf" -link_class="link"/>
		<lstElt42
		-str1="ft_printf" -str2="validé" -str3="23 Nov 2024" -str4="100/100"
		-str5="https://github.com/Maxime-juncker/ft_printf" -link_class="link"/>
		<lstElt42
		-str1="fract-ol" -str2="validé" -str3="06 Jan 2025" -str4="116/100"
		-str5="https://github.com/Maxime-juncker/fractol" -link_class="link"/>
		<lstElt42
		-str1="minitalk" -str2="validé" -str3="10 Jan 2025" -str4="125/100"
		-str5="https://github.com/Maxime-juncker/minitalk" -link_class="link"/>
		<lstElt42
		-str1="push_swap" -str2="validé" -str3="16 Jan 2025" -str4="100/100"
		-str5="https://github.com/Maxime-juncker/push_swap" -link_class="link"/>
		<lstElt42
		-str1="philosophers" -str2="validé" -str3="31 Mar 2025" -str4="100/100"
		-str5="https://github.com/Maxime-juncker/philosophers" -link_class="link"/>
		<lstElt42
		-str1="minishell" -str2="validé" -str3="24 Mar 2025" -str4="125/100"
		-str5="https://github.com/Maxime-juncker/Minishell" -link_class="link"/>
		<lstElt42
		-str1="miniRT" -str2="validé" -str3="07 Mai 2025" -str4="125/100"
		-str5="https://github.com/abidolet/miniRT" -link_class="link"/>

		<p><br></p>

		<div>
			<span>~/</span>
			<span style="color: #B982B6;">mjuncker</span>
			<span>/</span>
			<span style="color: #53C3F3;">home</span>
			<span>/</span>
			<span style="color: #FFFF34;">42_projects</span>/>
			<span>cd ..</span>
		</div>

		<div>
			<span>~/</span>
			<span style="color: #B982B6;">mjuncker</span>
			<span>/</span>
			<span style="color: #53C3F3;">home</span>/>
			<span>cd solo_projects && ls</span>
		</div>

		<div>
			<span>~/</span>
			<span style="color: #B982B6;">mjuncker</span>
			<span>/</span>
			<span style="color: #53C3F3;">home</span>
			<span>/</span>
			<span style="color: #FFFF34;">solo_projects</span>/>
		</div>
		<p><br></p>
		<lstElt42 -str1="name" -str2="desc" -str3="last_updated" -str4="language" -str5="link"/>
		<lstElt42 -str1="----" -str2="----" -str3="----" -str4="----" -str5="----"/>
		<lstElt42
		-str1="libunit" -str2="tester c++ modulaire" -str3="28 Jan 2025" -str4="c++"
		-str5="https://github.com/Maxime-juncker/better-libunit.git" -link_class="link"/>
		<lstElt42
		-str1="push swap tester" -str2="tester" -str3="20 Jan 2025" -str4="c"
		-str5="https://github.com/Maxime-juncker/push_swap_tester" -link_class="link"/>
		<lstElt42
		-str1="HumanSI" -str2="concours de la nsi (2nd)" -str3="18 Nov 2023" -str4="python"
		-str5="https://github.com/Maxime-juncker/HumanSI" -link_class="link"/>
		<lstElt42
		-str1="Maximatron" -str2="app de prise de note" -str3="15 Nov 2023" -str4="c#"
		-str5="https://github.com/Maxime-juncker/Maximatron" -link_class="link"/>
		<lstElt42
		-str1="Vulkouch" -str2="implementation de Vulkan" -str3="6 Mar 2024" -str4="c++"
		-str5="https://github.com/Maxime-juncker/Vulkouch" -link_class="link"/>
		<p><br></p>

		<div>
			<span>~/</span>
			<span style="color: #B982B6;">mjuncker</span>
			<span>/</span>
			<span style="color: #53C3F3;">home</span>
			<span>/</span>
			<span style="color: #FFFF34;">solo_projects</span>/>
			<span class="cursor">_</span>
		</div>
	</div>
</template>

<style scoped>

.project-42
{
	display: flex;
	flex-direction: column;
	justify-content: start;
	align-items: start;
	width: 100%;
	border: solid black 2px;
}

.project-42 header
{
	display: flex;
	flex-direction: row;
	justify-content: space-around;
	align-items: start;
	width: 100%;
}

</style>