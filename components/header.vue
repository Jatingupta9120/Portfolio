<template>
    <div
        class="flex justify-center bg-[#15103031] sticky top-0 z-40 bg-opacity-40 backdrop-filter backdrop-saturate-150 backdrop-blur-xl firefox:bg-opacity-100">
        <div class="w-full 2xl:w-10/12 2xl:max-w-screen-2xl mx-4">
            <div class="flex justify-between items-center py-3 ">
                    <img loading="lazy" src="/images/logo.svg" alt="logo" class="absolute h-10  sm:h-12 sm:mr-52 md:ml-12 lg:ml-20">
                    <div class="h-8 sm:mr-52 md:mr-60 lg:ml-20"/>
                <ul class="flex absolute right-0 mr-4">
                    <li v-for="item in headerItems" :key="item.name">
                        <a :href="item.url" class="flex mr-2 items-center justify-center hover:bg-gradient-to-r from-[#05abcd] via-[#6665cd] to-[#af1db7] rounded-full" target="_blank"
                            rel="noopener noreferrer">
                            <img loading="lazy" :src="item.icon"
                                class="max-h-10 w-auto" alt="icon" />
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
const headerItems = [
    {
        name: 'Github',
        url: "https://github.com/Jatingupta9120",
        icon: "/images/socials/github.png",
    },
    {
        name: 'LinkedIn',
        url: "https://www.linkedin.com/in/jatin-gupta9120/",
        icon: "/images/socials/linkedin.png",
    },
    {
        name: 'Twitter',
        url: "https://twitter.com/jatingupta9905",
        icon: "/images/socials/twitter.png",
    }
];

</script>