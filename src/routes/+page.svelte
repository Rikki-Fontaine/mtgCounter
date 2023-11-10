<script>
	import Counter from "../components/counter.svelte";
	import heart from "$lib/heart.png"
	import poison from "$lib/poison.png"
	import medal from "$lib/commdmedal.png"
</script>

<div class="mt-10 border border-black bg-gradient-to-br">
	<div class="flex justify-center gap-4 mb-5">
		<Counter bgColor = "bg-secondary-500" imagesrc={heart} counterBg="bg-red-600"/>
		<Counter bgColor = "bg-primary-600" imagesrc={poison} counterBg="bg-green-600"/>
	</div>

	<div class="flex justify-center gap-6">
		<Counter bgColor = "bg-tertiary-600" imagesrc={medal} counterBg="bg-purple-700"/>
		<Counter bgColor = "bg-success-800" imagesrc={medal} counterBg="bg-yellow-700"/>
		<Counter bgColor = "bg-warning-600" imagesrc={medal} counterBg="bg-emerald-700"/>
	</div>
</div>