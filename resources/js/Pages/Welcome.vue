<script setup>
import { Head, Link } from '@inertiajs/vue3';

defineProps({
    canLogin: {
        type: Boolean,
    },
    canRegister: {
        type: Boolean,
    },
    laravelVersion: {
        type: String,
        required: true,
    },
    phpVersion: {
        type: String,
        required: true,
    },
});

function handleImageError() {
    document.getElementById('screenshot-container')?.classList.add('!hidden');
    document.getElementById('docs-card')?.classList.add('!row-span-1');
    document.getElementById('docs-card-content')?.classList.add('!flex-row');
    document.getElementById('background')?.classList.add('!hidden');
}
</script>
<style scoped>
.st0 {
    fill: #ffffff;
}
</style>
<template>
    <div class="flex items-center justify-center min-h-screen bg-gray-100">
        <div
            class="flex flex-col items-center w-screen min-h-screen p-6 shadow-lg bg-gradient-to-b from-purple-900 via-slate-900 to-gray-900 rounded-2xl">
            <Link :href="'/'">
            <h1 class="flex items-center justify-center mb-4 space-x-1 text-5xl font-bold text-center text-white">
                <span>Twansa</span>
                <svg class="w-8 h-8 mt-1" version="1.1" id="_x32_" xmlns="http://www.w3.org/2000/svg"
                    xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 512 512" xml:space="preserve" fill="#ffffff"
                    stroke="#ffffff">
                    <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
                    <g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g>
                    <g id="SVGRepo_iconCarrier">

                        <g>
                            <path class="st0"
                                d="M510.069,388.114V70.633V3.268l-65.848,14.204L110.483,92.396h-0.01v262.876
                c-12.625-1.872-26.132-1.332-39.711,2.03c-48.156,11.924-78.972,54.796-68.83,95.756s57.403,64.499,105.559,52.575
                c48.156-11.924,78.972-54.796,68.83-95.756V182.327l267.901-60.733v211.914c-12.625-1.872-26.132-1.332-39.712,2.03
                c-48.156,11.924-78.972,54.796-68.83,95.756s57.403,64.499,105.559,52.575C489.395,471.946,520.211,429.075,510.069,388.114z">
                            </path>
                        </g>
                    </g>
                </svg>
                <span>usic</span>
            </h1>
            </Link>
            <div class="flex flex-col items-center justify-center flex-grow w-full md:flex-row">
                <div class="justify-end flex-grow w-full md:w-1/2">
                    <p class="px-4 mb-6 text-sm text-center text-white">A Light and Fast Spotify Playlist Maker and
                        Player
                    </p>
                    <div class="flex justify-center mb-6">
                        <img src="/storage/bg-1.png" alt="Illustration" class="object-contain w-full h-48 md:h-96">
                    </div>
                </div>
                <div class="flex-grow w-full md:w-1/2">
                    <h2 class="mb-4 text-2xl font-semibold text-center text-white">It's Free and Easy to Use</h2>
                    <div class="mb-4 text-center text-white">Login with:</div>
                    <div class="flex justify-center mb-6 space-x-4">
                        <div
                            class="relative p-4 transition-all bg-transparent rounded-lg shadow-md cursor-pointer shadow-sky-500 hover:shadow-sm hover:translate-y-1">
                            <p class="ml-2 text-xl text-white">Spotify</p>
                        </div>
                        <div
                            class="relative p-4 transition-all bg-transparent rounded-lg shadow-md cursor-pointer shadow-purple-500 hover:shadow-sm hover:translate-y-1">
                            <p class="ml-2 text-xl text-white">Google</p>
                        </div>
                    </div>
                    <div class="mb-4 text-center text-white">
                        <a href="/register" class="underline hover:text-gray-300">Or: Create My Account</a>
                    </div>
                    <div class="text-center text-white">
                        <a href="/login" class="underline hover:text-gray-300">Login with Email</a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>