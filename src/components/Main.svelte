<script>
    import Step from "./Step.svelte";

    let steps = [
        {name: 'High School Degree', icon: 'fa-solid fa-graduation-cap'},
        {name: 'Bachelors Degree', icon: 'fa-solid fa-graduation-cap'},
        {name: 'DNA-Technology', icon: 'fa-solid fa-dna'},
        {name: 'Pharmacology & Toxicology', icon: 'fa-solid fa-flask'},
        {name: 'Microbiology', icon: 'fa-solid fa-bacteria'},
        {name: 'Data Science & Bioinformatics', icon: 'fa-solid fa-chart-line'},
    ];

    let benefits = [
        {name: 'Eager to learn new things',
            description: '## long description ##'},
        {name: 'A team player',
            description: '## long description ##'},
        {name: 'Very good in the lab',
            description: '## long description ##'},
        {name: 'A self thought programmer',
            description: '## long description ##'},
    ]

</script>

<main class="flex flex-col flex-1 p-4">
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
        <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                Hi! I'm <span class="poppins text-blue-400">Ben Melis</span><br/>
                Pharmaceutical & Biological <span class="poppins text-blue-400">Scientist</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                My <span class="poppins text-blue-400">interests</span> are DNA-Technology (PCR, NGS, CRISPR),
                Toxicology & Pharmacology, Bioinformatics and much more.
            </p>
        </div>
        <div class="relative shadow-2xl grid place-items-center">
            <img src={"images/profile.png"}
                 alt="Profile"
                 class="object-cover z-[2] max-h-[70vh]"/>
        </div>
        <div class="flex flex-col gap-2 text-center sm:col-span-2 pt-20">
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Languages
            </h3>
            <div class="flex flex-col items-center pt-10 sm:pt-14 md:pt-18 lg:pt-24">
                <p class="text-2xl md:text-3xl lg:text-4xl text-blue-400">Dutch
                    <span class="text-base sm:text-lg md:text-xl">(native)</span></p>
                <div class="mt-2 h-2 w-[12rem] sm:w-[16rem] md:w-[20rem] bg-gray-500 rounded-full"/>
                <p class=" mt-12 text-2xl md:text-3xl lg:text-4xl text-blue-400">English</p>
                <div class="mt-2 h-2 w-[12rem] sm:w-[16rem] md:w-[20rem] bg-gray-500 rounded-full"/>
            </div>
        </div>
    </section>
    <section id="education" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center">
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Education
            </h3>
        </div>
        <div class="grid grid-cols-1 gap-12 lg:gap-10 text-md sm:text-lg md:text-xl">
            <Step step={steps[0]}>
                <p>
                    <strong class="text-blue-400">School:</strong> KSD Diest<br/>
                    <strong class="text-blue-400">Degree:</strong> Math & Sciences<br/>
                    <strong class="text-blue-400">Year of graduation:</strong> 2020
                </p>
            </Step>
            <Step step={steps[1]}>
                <p>
                    <strong class="text-blue-400">School:</strong> UCLL (Association KULeuven)<br/>
                    <strong class="text-blue-400">Degree:</strong> Bachelor degree in Pharmaceutical and Biological
                    Laboratory Techniques<br/>
                    <strong class="text-blue-400">Year of graduation:</strong> 2025 (expected)
                </p>
            </Step>
        </div>
        <div class="flex flex-col gap-2 text-center">
            <h3 class="font-semibold text-2xl sm:text-3xl md:text-4xl">
               Relevant Courses
            </h3>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-2 gap-12 lg:gap-10 lg:text-xl">
            <Step step={steps[2]}>
                <p>
                    Personally, this was one of my <b class="text-blue-400"> favorite</b> courses in college.
                    I really enjoyed working in the lab here since you can really see the theory play into practice.
                    I've gathered important and interesting knowledge over the course of these laboratory sessions such
                    as working with a <b class="text-blue-400">qPCR</b> machine, using <b class="text-blue-400">Oxford
                    Nanopore Sequencing</b> techniques, <b class="text-blue-400">Gel Electrophoresis</b>,
                    <b class="text-blue-400">CRISPR</b> and much more. I can't wait to get more hands on practice with
                    these amazing technologies.
                </p>
            </Step>
            <Step step={steps[3]}>
                <p>
                    I found this the <b class="text-blue-400">most interesting</b> of all the courses that
                    I took. Learning how drugs affect the human body in good and bad ways was extremely interesting.
                    During this course I gathered extensive knowledge on the <b class="text-blue-400">
                    biochemical pathways</b> drugs undergo in the body to give the expected effects and
                    side-effects, as well as the ins and outs of the extensive research that goes on during the
                    <b class="text-blue-400"> drug development phases</b> and how important they are. I
                    hope to gather a lot more knowledge about these subjects during my career.
                </p>
            </Step>
            <Step step={steps[4]}>
                <p>
                    This was by far the largest course I took. I learned a lot about the different categories of
                    <b class="text-blue-400">micro-organisms</b>, how they respond to the environment and how they
                    interact with other organisms like animals or plants. I learned how to work with micro-organisms
                    in a <b class="text-blue-400">controlled and sterile</b> laboratory environment, how to culture
                    them and how to perform <b class="text-blue-400">various biochemical tests</b>.
                </p>
            </Step>
            <Step step={steps[5]}>
                <p>
                    This course was not very popular among students, most found it boring and unuseful. I was one of
                    those people at the start of college but along the way I got very interested in
                    <b class="text-blue-400">data analysis and statistics</b> and learned how important this all is in
                    the medical field. During these courses I gathered a lot of knowledge about tools like
                    <b class="text-blue-400">BLAST</b>, <b class="text-blue-400"> Clustal Omega</b> and
                    <b class="text-blue-400"> Primer3D</b> for dealing with sequenced data. Using databases like NCBI,
                    GenBank and UniProt was also one of the core subjects we tackled during this course.
                </p>
            </Step>
        </div>
    </section>
    <section id="about"
             class="py-20 pt-18 lg:pt-20 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative">
        <div
                class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3
                before:h-1.5 before:bg-blue-400 after:absolute after:bottom-0 after:right-0 after:w-2/3
                after:h-1.5 after:bg-blue-400 py-4">
            <h6 class="text-lg sm:text-xl md:text-2xl">Want to know more?</h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                A bit <span class="poppins text-blue-400">about</span> me.
            </h3>
        </div>
        <p class="mx-auto poppins font-semibold text-xl sm:text-2xl md:text-3xl">I am . . .</p>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
            {#each benefits as benefit, index}
                <div class="flex gap-6 sm:gap-8">
                    <p class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold">
                        0{index + 1}
                    </p>
                    <div class="flex flex-col gap-6 sm:gap-8">
                        <h3 class="text-2xl sm:text-3xl md:text-5xl">
                            {benefit.name}
                        </h3>
                        <p>{benefit.description}</p>
                    </div>
                </div>
            {/each}
        </div>
        <h5 class="poppins text-2xl sm:text-3xl font-semibold text-center">
            The <span class="poppins text-blue-400">Complete</span> Package
        </h5>
        <div class="flex flex-col overflow-x-scroll gap-10 max-w-[800px] mx-auto w-full">
            <table class="bg-white text-slate-700 rounded text-center">
                <thead class="border-b border-solid border-slate-200">
                    <tr class="">
                        <th />
                        <th class="whitespace-nowrap bg-blue-400 text-white p-4 px-8">Candidate #1</th>
                        <th class="whitespace-nowrap bg-blue-400 text-white p-4 px-8">Candidate #2</th>
                        <th class="whitespace-nowrap bg-blue-400 text-white p-4 px-8">Candidate #3</th>
                        <th class="whitespace-nowrap bg-blue-400 text-white p-4 px-8">Me</th>
                    </tr>
                </thead>
                <tbody>
                    <tr class="border-b border-solid border-slate-200">
                        <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold
                            text-sm whitespace-nowrap">Eager To Learn</td>
                        <td><i class="fa-solid fa-check text-slate-500"/></td>
                        <td><i class="fa-solid fa-xmark text-slate-500"/></td>
                        <td><i class="fa-solid fa-check text-slate-500"/></td>
                        <td><i class="fa-solid fa-check text-green-500"/></td>
                    </tr>
                    <tr class="border-b border-solid border-slate-200">
                        <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold
                            text-sm whitespace-nowrap">Orderly</td>
                        <td><i class="fa-solid fa-check text-slate-500"/></td>
                        <td><i class="fa-solid fa-check text-slate-500"/></td>
                        <td><i class="fa-solid fa-xmark text-slate-500"/></td>
                        <td><i class="fa-solid fa-check text-green-500"/></td>
                    </tr>
                    <tr class="border-b border-solid border-slate-200">
                        <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold
                            text-sm whitespace-nowrap">Communication Skills</td>
                        <td><i class="fa-solid fa-xmark text-slate-500"/></td>
                        <td><i class="fa-solid fa-check text-slate-500"/></td>
                        <td><i class="fa-solid fa-check text-slate-500"/></td>
                        <td><i class="fa-solid fa-check text-green-500"/></td>
                    </tr>
                    <tr class="border-b border-solid border-slate-200">
                        <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold
                            text-sm whitespace-nowrap">GLP</td>
                        <td><i class="fa-solid fa-check text-slate-500"/></td>
                        <td><i class="fa-solid fa-xmark text-slate-500"/></td>
                        <td><i class="fa-solid fa-check text-slate-500"/></td>
                        <td><i class="fa-solid fa-check text-green-500"/></td>
                    </tr>
                    <tr class="border-b border-solid border-slate-200">
                        <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold
                            text-sm whitespace-nowrap">Programming Ability</td>
                        <td><i class="fa-solid fa-xmark text-slate-500"/></td>
                        <td><i class="fa-solid fa-check text-slate-500"/></td>
                        <td><i class="fa-solid fa-xmark text-slate-500"/></td>
                        <td><i class="fa-solid fa-check text-green-500"/></td>
                    </tr>
                </tbody>
            </table>
        </div>
        <div class="mx-auto -mt-12 italic sm:hidden opacity-50">
            <p>Scroll to see more &rarr;</p>
        </div>
        <p class="mx-auto">Why not invest?</p>
    </section>
</main>