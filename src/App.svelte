<script>
    import AboutModal from './lib/AboutModal.svelte'
    import { isModalOpen } from './store'
</script>

<main
    class="h-screen p-0 m-0 font-mono text-white bg-slate-900"
    id="background-pattern"
>
    <AboutModal />
    <div class="flex flex-col items-center justify-center w-full h-screen">
        <!-- big text -->
        <h1 class="splrge-title">
          SPLRGE
        </h1>
        <!-- -->
        
        <div class="flex space-x-4 leading-loose text-zinc-300">
          <button
            class="homeButton"
            on:click={() => isModalOpen.set(true)}
        >
            About us
        </button>
        <div class="border-l-2 border-white"></div>
        <button
            class="homeButton"
            on:click={() => window.location.href = 'https://discord.splrge.dev'}
        >
            Join our Discord
      </button>
        </div>
    </div>
</main>

<style>
    #background-pattern {
        position: relative;
        overflow: hidden;
        z-index: 1;
    }
    #background-pattern:before {
        z-index: -1;
        position: absolute;
        left: 0;
        top: 0;
        content: url('/background.png');
        opacity: 0.4;
    }
</style>
