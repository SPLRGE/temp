<script>
    import { isModalOpen } from "../store";

    let modalOpen = false;

    isModalOpen.subscribe(value => {
        modalOpen = value;
    });

</script>


{ #if modalOpen }
    <div class="fixed bottom-0 z-50 grid h-screen w-full place-items-center bg-opacity-50 backdrop-blur-md bg-plack">
        <!-- Modal -->
        <div class="w-full max-w-md rounded-lg bg-slate-950">
            <div class="flex items-center justify-between p-4 text-3xl">
                <span class="font-bold">About us</span>
                <button on:click={ () => isModalOpen.set(false)}>
                    &times;
                </button>
            </div>
            <hr />
            <div class="flex flex-col px-4 py-2 text-zinc-400 space-y-2">
                <p>
                    <a href="https://github.com/splrge/create-ts-app" class="font-bold underline hover:text-white" target="_blank">splrge/create-ts-app</a>
                    Easily create a Typescript project.
                </p>
                <p>
                    <a href="https://github.com/splrge/temp" class="font-bold underline hover:text-white" target="_blank">splrge/temp</a>
                    This website. Made with svelte.
                </p>
                <hr class="my-4" />
                <a href="https://github.com/splrge" class="underline hover:text-white" target="_blank">Github</a>
                <a href="mailto:hello@splrge.dev" class="underline hover:text-white">hello@splrge.dev</a>
            </div>
        </div>
    </div>
{/if}