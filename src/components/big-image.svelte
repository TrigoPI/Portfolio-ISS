<script lang="ts">
    export let link: string;
    export let title: string;
</script>

<div class="relative w-screen h-screen flex flex-col gap-8 items-center justify-center overflow-hidden" style="background-image: url({link});">
    <h1 class="slide-in-top text-5xl text-center font-bold sm:text-9xl text-white">{ title }</h1>
</div>