<script>
    export let y;

    let tabs = [
        {name: 'Education', link: '#education'},
        {name: 'About me', link: '#about'},
    ];

    let openMenu = false;
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
    <a href="#linkedin"
       target="_blank"
       class="blueShadow relative overflow-hidden px-5 py-2 group rounded-full bg-white text-slate-950">
        <div class="absolute top-0 right-full w-full h-full bg-blue-400 opacity-20 group-hover:translate-x-full
        z-0 duration-200"/>
        <h4 class="relative z-[9]">Get in touch</h4>
    </a>
</header>