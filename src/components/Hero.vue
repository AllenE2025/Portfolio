<template>
    <div class="text-center bg-neutral-900 p-8 rounded-xl relative overflow-hidden shadow-lg">
        <div class="pointer-events-none absolute top-0 left-0 right-0 h-0.75
        bg-linear-to-b
        from-white/10
        to-transparent
        ">
        </div>
        <div class="absolute bottom-0 left-0 right-0 h-0.75 bg-linear-to-t from-black/50 to-transparent
        "></div>
        <h1
            class="text-5xl md:text-6xl font-extrabold mb-4 bg-clip-text text-transparent bg-linear-to-b from-white/60 via-yellow-400 to-yellow-600">
            Hi, I'm David Allen</h1>

        <div class="relative bg-neutral-800 overflow-hidden rounded-md p-4 mb-4 shadow-inner">
            <!-- Top gradient -->
            <div
                class="absolute top-0 left-0 right-0 h-1 bg-linear-to-t from-transparent to-black/60 pointer-events-none">
            </div>
            <!-- Bottom gradient -->
            <div
                class="absolute bottom-0 left-0 right-0 h-1 bg-linear-to-b from-transparent to-black/60 pointer-events-none">
            </div>
            <!-- Left gradient -->
            <div
                class="absolute top-0 bottom-0 left-0 w-1 bg-linear-to-l from-transparent to-black/60 pointer-events-none">
            </div>
            <!-- Right gradient -->
            <div
                class="absolute top-0 bottom-0 right-0 w-1 bg-linear-to-r from-transparent to-black/60 pointer-events-none">
            </div>
            <p class="text-lg md:text-xl text-gray-300 tracking-wide">
                This portfolio was made using
                <span
                    class="text-green-500 font-medium transition-all inline-block hover:scale-105 active:text-green-600">
                    <a href="https://vuejs.org" target="_blank" rel="noopener noreferrer">Vue</a>
                </span>,
                <span
                    class="text-blue-300 font-medium transition-all inline-block hover:scale-105 active:text-blue-400">
                    <a href="https://tailwindcss.com" target="_blank" rel="noopener noreferrer">Tailwind CSS</a>
                </span>,
                <span
                    class="text-blue-200 font-medium transition-all inline-block hover:scale-105 active:text-blue-300">
                    <a href="https://iconify.design" target="_blank" rel="noopener noreferrer">Iconify</a>
                </span>,
                <span
                    class="text-purple-300 font-medium transition-all inline-block hover:scale-105 active:text-purple-400">
                    <a href="https://trycolorlab.com" target="_blank" rel="noopener noreferrer">ColorLab</a>
                </span> and
                <span
                    class="text-gray-400 font-medium transition-all inline-block hover:scale-105 active:text-gray-500">
                    <a href="https://vercel.com/home" target="_blank" rel="noopener noreferrer">Vercel</a>
                </span>
            </p>
        </div>


        <a href="#projects"
            class="inline-block p-3 rounded-md bg-yellow-500 text-black font-medium transition-all hover:scale-105 active:scale-95 active:bg-yellow-600 relative overflow-hidden shadow-md hover:shadow-lg">
            View My Projects
            <div
                class="pointer-events-none absolute bg-linear-to-t from-yellow-900 to-transparent bottom-0 left-0 right-0 h-0.75">
            </div>
        </a>

    </div>
</template>
