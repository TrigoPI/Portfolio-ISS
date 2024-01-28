<script lang="ts">
	import type { IconDefinition } from "@fortawesome/free-solid-svg-icons";
    import Fa from "svelte-fa";

    export let title: string;
    export let link: string;
    export let icon: IconDefinition; 

</script>

<a 
    href={ link }
    class="flex flex-col items-center gap-4 rounded-md px-12 py-8 shadow-lg duration-150 hover:scale-110"
>
    <div class="px-4 text-2xl border-b flex-1">
        <h1 class="text-center py-2">{ title }</h1>
    </div>
    <div class="text-3xl py-4">
        <Fa icon={ icon } />
    </div>
</a>