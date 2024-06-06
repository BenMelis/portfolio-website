<script lang="ts">
    export let y: any;

    let tabs = [
        {name: 'Education', link: '#education'},
        {name: 'About me', link: '#about'},
    ];

    let popupOpen = false;

    function closePopup(event) {
        if (event.target.className === 'popup') {
            popupOpen = false;
        }
    }

</script>

<header class={"sticky z-[10] top-0 duration-200 px-6 flex items-center justify-between border border-solid" + (
    y > 0 ? ' py-4 bg-slate-950 border-blue-600': ' py-6 bg-transparent border-transparent')}>
    <h1 class="font-medium">
        <b class="font-bold poppins">Ben</b> Melis
    </h1>
    <div
      class="flex sm:hidden gap-4 ml-auto px-1 m-1 border border-white rounded hover:cursor-pointer hover:text-blue-400
      hover:border-blue-400">
        <a href="#education"><i class="fa-solid fa-graduation-cap"/><a/>
    </div>
    <div
      class="flex sm:hidden gap-4 px-1 m-1 border border-white rounded hover:cursor-pointer hover:text-blue-400
      hover:border-blue-400">
        <a href="#about"><i class="fa-solid fa-user"/><a/>
    </div>
    <div class="sm:flex hidden gap-4 ml-auto pr-2">
        {#each tabs as tab, index}
            <a href={tab.link} class="duration-200 hover:text-blue-400">
                <p>{tab.name}</p>
            </a>
        {/each}
    </div>
    <button on:click={() => popupOpen = true}
       class="blueShadow relative overflow-hidden px-5 py-2 group rounded-full bg-white text-slate-950">
        <div class="absolute top-0 right-full w-full h-full bg-blue-400 opacity-20 group-hover:translate-x-full
        z-0 duration-200"/>
        <h4 class="relative z-[9]">Get in touch</h4>
    </button>
    {#if popupOpen}
        <div class="popup fixed inset-0 flex items-center justify-center bg-black bg-opacity-50"
             on:click={closePopup}>
            <div
              class="bg-slate-800 p-4 rounded-lg shadow-lg flex flex-col items-center w-[80%] h-[45%] sm:h-[60%] max-w-[500px] max-h-[450px]">
                <button
                  class="self-end border border-white hover:cursor-pointer hover:border-blue-400 hover:text-blue-400 rounded px-2"
                        on:click={() => popupOpen = false}>
                    <i class="fa-solid fa-x"></i>
                </button>
                <div class="text-xl sm:text-2xl md:text-3xl flex flex-col">
                    <p class="text-base md:text-2xl pt-6 md:pt-8 lg:pt-10"><b class="pr-2">Email</b><br/>
                        ben.melis25@outlook
                        .com</p>
                    <a href="https://www.linkedin.com/in/ben-melis-2a5406312"
                       target="_blank" class="py-6 md:py-8 lg:py-10 hover:text-blue-400 hover:cursor-pointer">
                        <i class="fa-brands fa-linkedin"/><br/> LinkedIn
                    </a>
                    <a href="https://github.com/BenMelis"
                       target="_blank" class="pb-6 md:pb-8 lg:pb-10 hover:text-blue-400 hover:cursor-pointer">
                        <i class="fa-brands fa-github"/><br/> GitHub
                    </a>
                </div>
            </div>
        </div>
    {/if}
</header>