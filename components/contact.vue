<script lang="ts" setup>
let loading: any;
const socials = [
    {
        name: 'Email',
        url: "mailto:jatinofficial9120@gmail.com",
        icon: "/images/socials/mail.png",
        username: '@Jatin99'
    },
    {
        name: 'Twitter',
        url: "https://twitter.com/jatingupta9905/",
        icon: "/images/socials/twitter.png",
        username: 'Jatin99'
    },
    {
        name: 'Github',
        url: "https://github.com/Jatingupta9120/",
        icon: "/images/socials/github.png",
        username: 'Jatin99'
    },
    {
        name: 'LinkedIn',
        url: "https://www.linkedin.com/in/jatin-gupta9120/",
        icon: "/images/socials/linkedin.png",
        username: 'Jatin99'
    },
    {
        name: 'Discord',
        url: "https://discordid.netlify.app/?id=jatin99",
        icon: "/images/socials/discord.png",
        username: 'Jatin99'
    }
]
</script>
<template>
    <div>
        <h3 v-motion-slide-visible-top class="heading my-8 sm:my-24">Contacts
        </h3>
        <div v-motion-slide-visible-bottom class="sm:mt-12 w-full">
            <div class="bg-[#15103088] card blurblur brdr">
                <p class="headingTitle">
                    Get in touch</p>
                <form action="" class="mt-12 flex flex-col gap-8">
                    <label class="flex flex-col">
                        <span class="text-white font-medium mb-4">Your Name</span>
                        <input type='text' name='name' placeholder="What's your good name?" class="inputBox" />
                    </label>
                    <label class="flex flex-col">
                        <span class="text-white font-medium mb-4">Your email</span>
                        <input type='email' name='email' placeholder="What's your web address?" class="inputBox" />
                    </label>
                    <label class="flex flex-col">
                        <span class="text-white font-medium mb-4">Your Message</span>
                        <textarea rows={7} name='message' placeholder='What you want to say?' class="inputBox" />
                    </label>

                    <button type='submit' class="btn">
                        {{ loading ? "Sending..." : "Send" }}
                    </button>
                </form>
            </div>
        </div>
        <div v-motion-slide-visible-bottom class=" sm:mt-12  w-full font-mono">
            <div $VanillaTilt data-tilt class="brdr card-color card">
                <div class="inner blurblur">
                    <p class="headingTitle">
                        Socials</p>
                    <div class="box" v-for="item in socials" :key="item.name">
                        <div class="smlbox">
                            <h1 class="sm:text-2xl text-pink-500">{{ item.name }}</h1>
                        </div>
                        <div class="smlbox">
                            <a :href="item.url"
                                class=" underline-offset-4 decoration-2 underline flex items-center sm:text-xl text-sky-300 justify-center"
                                target="_blank" rel="noopener noreferrer">
                                <img loading="lazy" :src="item.icon" class="h-8 sm:max-h-10 w-auto mx-auto hover:border-b-2 hover:border-sky-300" alt="icon">
                            </a>
                        </div>
                        <div class="smlbox">
                            <a :href="item.url"
                                class=" underline-offset-4 decoration-2 underline flex items-center sm:text-xl text-sky-300 justify-center hover:decoration-pink-500"
                                target="_blank" rel="noopener noreferrer">
                                {{ item.username }}
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<style scoped>
.card {
    @apply my-4 sm:my-0 lg:w-3/5 mx-auto text-center rounded-2xl md:w-11/12;
    transform-style: preserve-3d;
}
.inner {
    @apply w-full sm:p-8;
}

.inner:hover {
    transform: translateZ(80px);
    transform: scale3d(50px);
}
.headingTitle {
    @apply sm:text-[18px] text-[14px] text-center text-violet-500 uppercase tracking-wider font-sans font-bold sm:m-0 mt-4;
}

.inputBox {
    @apply bg-[#151030] py-4 px-6 placeholder:text-[#aaa6c3] text-white rounded-lg outline-none border-none font-medium w-[90%] mx-auto;
}

.btn {
    @apply bg-[#151030] mb-2 py-3 px-8 mx-auto rounded-xl outline-none w-2/5 text-white font-bold shadow-md shadow-[#050816];
}

form ::placeholder {
    text-align: center;
}

input {
    text-align: center;
}

.box {
    @apply text-white text-center font-bold mt-4 w-full px-10 rounded-3xl mx-auto flex items-center justify-between;
}

.smlbox {
    @apply w-1/3 text-center;
}</style>
