<script>
    import Step from "./Step.svelte";

    let steps = [
        {
            name: 'Smoljames Store',
            icon: 'fa-solid fa-cart-shopping',
        },
        {
            name: 'Ultimate Todos',
            icon: 'fa-solid fa-list-check',
        },
        {
            name: 'Pokedex',
            icon: 'fa-solid fa-diagram-project',
        },
    ];
</script>

<main class="flex flex-col flex-1 p-4">
    <section
        id="introPage"
        class="grid grid-cols-1 lg:grid-col-2 gap-10 py-8 sm:py-14"
    >
        <div
            class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10"
        >
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                Hi! I'm <span class="poppins text-violet-400">Robert</span>
                Ramirez <br />
                Full Stack
                <span class="poppins text-violet-400">Developer</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                My <span class="text-violet-400">favorite tech</span> includes JavaScript/TypeScript
                (NextJs or SvelteKit for React/Svelte), TailwindCSS, Node.Js + Express,
                and MongoDB, PostgreSQL and Firebase for Databases.
            </p>
            <a
                href="www.linkedin.com/in/roberto-ramirez-aguilar"
                target="_blank"
                class="blueShadow mx-auto lg:mr-auto text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer"
            >
                <div
                    class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
                />
                <h4 class="relative z-9">Get in touch</h4>
            </a>
        </div>
        <div class="relative shadow-2xl grid place-items-center">
            <img src={"images/profile.png"} alt="Robert Ramirez profile" class="object-cover z-[2] max-h-[70vh]">
        </div>
    </section>
    <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-lg sm:text-xl md:text-2xl">
                A few of my creative endeavors
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Curious to <span class="poppins text-violet-400">see</span> my work?
            </h3>
        </div>
        <a href="https://github.com/Robertron624?tab=repositories" target="_blank" class="mx-auto px-4 py-2 rounded-md border border-white border-solid flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-violet-700 duration-200">
            <i class="fa-regular fa-circle-pay"></i>
            <p>
                Enter my <span class="text-blue-700 font-semibold">Github</span>
            </p>
        </a>
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>
                    SmolJames Store is a full stack e-commerce application built with <strong class="text-violet-400">NextJs, TailwindCSS, and MongoDB</strong>. It features a fully functional shopping cart, user authentication, and a checkout process with Stripe.
                </p>
            </Step>
            <Step step={steps[1]}>
                <p>
                    Ultimate Todos is a full stack application built with <strong class="text-violet-400">SvelteKit, TailwindCSS, and Firebase</strong>. It features user authentication, a fully functional todo list, and a dark mode toggle.
                </p>
            </Step>
            <Step step={steps[2]}>
                <p>
                    Pokedex is a full stack application built with <strong class="text-violet-400">React, TailwindCSS, and PokeAPI</strong>. It features a fully functional pokedex with a search bar and a dark mode toggle.
                </p>
            </Step>
        </div>
    </section>
</main>
