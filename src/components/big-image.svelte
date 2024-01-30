<script lang="ts">
    export let link: string;
    export let title: string;
</script>

<div class="relative w-screen h-screen flex flex-col gap-8 items-center justify-center overflow-hidden" style="background-image: url({link});">
    <h1 class="slide-in-top text-5xl text-center sm:text-9xl p-20">{ title }</h1>
</div>

<style>    
    div {
        background-position: center;
    }

    div > h1 {
        background-color: white;
        backdrop-filter: blur(10px);
        mix-blend-mode: screen;
        font-family: 'Onest', sans-serif;
        font-weight: 900;
    }
</style>