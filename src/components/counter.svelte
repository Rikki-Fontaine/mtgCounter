<script>
    import heart from "$lib/heart.png"


    export let imagesrc = "";
    export let bgColor = "";
    export let counterBg = "";
</script>


<div class="flex justify-center">

    <div class="border border-black w-fit p-1 {bgColor} rounded-md">

        <div class="flex justify-center">
            <img src={imagesrc} alt="pixel heart" width=50 class="shadow-black border bg-orange-300 border-black shadow-inner">
        </div>   

        <div class="flex w-full justify-center"> 
            <div class="flex justify-center mt-5 w-fit">
                <button class="btn-sm variant-filled-error rounded-sm shadow-[0_1px_2px_4px_rgba(0,0,0,0.0)] shadow-black">-</button>
                <span class="m-2 text-lg font-[Audiowide] shadow-black {counterBg} p-2 border-2 border-black shadow-inner">20</span>
                <button class="btn-sm variant-filled-success rounded-sm shadow-[0_1px_2px_4px_rgba(0,0,0,0.0)] shadow-black">+</button>
            </div>
        </div>

    </div>

</div>