<script>
    import heart from "$lib/heart.png"


    export let imagesrc = "";
    export let bgColor = "";
    export let counterBg = "";
    export let textColor = "";

    export let count = 0;
</script>


<div class="flex justify-center">

    <div class="border-2 shadow-md shadow-black border-black w-fit p-1 {bgColor} rounded-md w-30">

        <div class="flex justify-center">
            <img src={imagesrc} alt="pixel heart" width=50 class="shadow-black border-4 bg-orange-300 border-black shadow-inner">
        </div>   

        <div class="flex w-full justify-center"> 
            <div class="flex justify-center mt-5 w-30">
                <button on:click={() => count -=1} class="btn-sm variant-filled-error rounded-sm shadow-[0_1px_2px_4px_rgba(0,0,0,0.0)] shadow-black">-</button>
                
                {#if count >= 10 || count < 0}
                    <span class="m-2 text-left w-12 text-lg font-[Audiowide] shadow-black {counterBg} p-1 border-2 border-black shadow-inner text-center {textColor}">{count}</span>
                {:else}
                    <span class="m-2 text-center w-12 text-lg font-[Audiowide] shadow-black {counterBg} p-1 border-2 border-black shadow-inner {textColor}">0{count}</span>
                {/if}
                <button on:click={() => count+=1} class="btn-sm variant-filled-success rounded-sm shadow-[0_1px_2px_4px_rgba(0,0,0,0.0)] shadow-black">+</button>
            </div>
        </div>

    </div>

</div>