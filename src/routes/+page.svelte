<script>
	import Counter from "../components/counter.svelte";
	import heart from "$lib/heart.png"
	import poison from "$lib/poison.png"
	import medal from "$lib/commdmedal.png"
</script>

<div class="border border-teal-600 rounded-full py-20 md:p-2">
	<div class="flex justify-center gap-4 mb-5">
		<Counter bgColor = "bg-neutral-300" imagesrc={heart} counterBg="bg-slate-800"/>
	</div>
	
	<div class="flex justify-around mb-5">
		<Counter bgColor = "bg-success-700" imagesrc={medal} counterBg="bg-red-700"/>
		<Counter bgColor = "bg-blue-600" imagesrc={poison} counterBg="bg-green-600"/>
	</div>

	<div class="flex justify-center gap-10 md:gap-40">
		<Counter bgColor = "bg-red-600" imagesrc={medal} counterBg="bg-blue-600"/>
		<Counter bgColor = "bg-slate-600" imagesrc={medal} counterBg="bg-neutral-300" textColor="text-black"/>
	</div>
</div>