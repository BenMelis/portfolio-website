<script lang="ts">
    export let step: any;
</script>

<div class="p-4 sm:p-8 flex flex-col gap-4 rounded-lg border border-solid border-blue-700 text-center group
     hover:border-blue-400 duration-200">
    <div class="bg-slate-950 grid place-items-center px-4 text-5xl md:text-6xl -mt-10 sm:-mt-12 md:-mt-14 lg:-mt-16
         mx-auto duration-200">
        <i class={step.icon} />
    </div>
    <h3 class="font-medium text-xl sm:text-2xl md:text-3xl">{step.name}</h3>
    <slot/>
</div>