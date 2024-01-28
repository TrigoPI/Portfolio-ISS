<script>
	import { base } from "$app/paths";
	import { faHome } from "@fortawesome/free-solid-svg-icons";
	import Fa from "svelte-fa";

</script>

<a 
    href="/"
    class="fixed top-0 left-0 p-4 z-50 text-2xl opacity-30 duration-150 hover:opacity-100 hover:scale-105 text-blue-400"
>
    <Fa icon={ faHome } />
</a>

<slot />