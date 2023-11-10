<script>
	import Counter from "../components/counter.svelte";
	import heart from "$lib/heart.png"
	import poison from "$lib/poison.png"
</script>

<Counter bgColor = "bg-secondary-500" imagesrc={heart} counterBg="bg-red-600"/>
<Counter bgColor = "bg-primary-600" imagesrc={poison} counterBg="bg-green-600"/>