<script>
import { isModalOpen } from "../store";

let modalOpen = false;

isModalOpen.subscribe(value => {
    modalOpen = value;
});

</script>


{ #if modalOpen }
<div class="fixed bottom-0 z-50 grid w-full h-screen bg-opacity-50 place-items-center bg-plack backdrop-blur-md">
    <!-- Modal -->
    <div class="w-full max-w-sm rounded-lg bg-slate-950">
        <div class="flex items-center justify-between p-4 text-2xl">
            <span class="font-bold">About us</span>
            <button on:click={ () => isModalOpen.set(false)}>
                &times;
            </button>
        </div>
        <hr />
        <p class="px-4 py-2 text-zinc-400">
            We are SPLRGE. We innovate in open-source by offering SAAS, libraries for all languages and customized development services for you. We use the latest technologies for our projects.
            <br /><br />
            <a href="https://github.com/splrge" class="underline hover:text-white" target="_blank">Github</a><br />
            <a href="mailto:hello@splrge.dev" class="underline hover:text-white">hello@splrge.dev</a>
        </p>
    </div>    
</div>
{/if}