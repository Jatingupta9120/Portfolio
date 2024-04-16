<script setup lang="ts">
const data = [
    {
        position: 'SDE Intern ',
        company: 'ITJOBXS',
        url: 'https://www.itjobxs.com/',
        time: '1 Nov 2023 - 1 Jan 2024',
        points: [
        "Worked on the Design and Development part of a fully responsive web page for a particular section of itjobxs.com",
        "Worked on User Verification/Authentication + Engineering challenges of detecting and removing the fake bots and posts",
        "Integrated Recaptcha with the website - Google Layer of Protection for websites"
        ],
        id: 1
    },
    
    {
        position: 'Amazon ML Summer School 2023',
        company: 'Amazon',
        url: 'https://www.amazon.science/news-and-features/third-annual-2023-ml-summer-school-amazon-india',
        time: '1 Sep 2023 - 1 Nov 2023',
        points: [
        "It was an integrated learning program for students on crucial Machine Learning (ML) topics including Supervised Learning, Deep Neural Networks, Dimensionality Reduction, Unsupervised Learning, Probabilistic Graphical Models, Sequential Learning, Causal Inference, and Reinforcement Learning"
        ],
        id: 2
    },
    {
        position: 'GCloud Study JAM Participant',
        company: 'Google Developer Student Clubs',
        url: 'https://www.cloudskillsboost.google/',
        time: '1 October 2022 - 30 October 2023',
        points: [
            "Completed Gen:Al Level and 8 Modules.",
            "Performed hands on experience on Lab and learnt different cloud computing concepts through videos."
        ],
        id: 3
    },
    {
        position: 'Open Source Contributor',
        company: 'Hacktoberfest',
        url: 'https://hacktoberfest.com/',
        time: '1 Oct 2023 - 1 Nov 2023',
        points: [
        "Contributed to open source projects in HACTOBERFEST-2023 using HTML, C, and Java programming.",
        "Raised 5 pull requests and got them merged",
        "Learned about Git and GitHub through the process"
        ],
        id: 4
    },
    {
        position: 'Web Development and Designing Intern',
        company: 'TECH-A-INTERN',
        url: 'https://techaintern.com/',
        time: '1 July 2023 - 1 Aug 2023',
        points: [
        "I have done three projects during this internship like weather-application , Todo App, Image-gallery-filtering",
        "Skills: Cascading Style Sheets (CSS) · JavaScript · HTML"
        ],
        id: 5
    },
    {
        position: 'IBM SkillsBuild 6 Weeks Internship for Emerging Technologies in Front End Development (FED) ',
        company: 'All India Council for Technical Education and Edunet Foundation with IBM',
        url: 'https://internship.aicte-india.org/',
        time: '1 June 2023 - 1 July 2023',
        points: [
        "I have successfully completed a Project Based", 
        "Learning/Internship under the IBM SkillsBuild program.",
        "It was a 6 Weeks Internship Program for Emerging Technologies in Front End Development (FED)."
        ],
        id: 6
    },
    {
        position: 'Web Development Intern',
        company: 'Code Clause',
        url: 'https://internship.codeclause.com/',
        time: '1 April 2023 - 1 May 2023',
        points: [
        "During my internship, I have worked on some project like developing a to-do list page and develop a movie website using front end Tech"
        ],
        id: 7
    },
    {
        position: 'Web Development Intern',
        company: 'letsgrowmore',
        url: 'https://letsgrowmore.in/',
        time: '1 Mar 2023 - 1 April 2023',
        points: [
        "I have successfully completed a Project Based", 
        "I have build some good web aplication project under this internship",
        "It was a Internship Program for Emerging Technologies in Web Development "
        ],
        id: 8
    },
    {
        position: 'Participant',
        company: 'The Arcade-Google Cloud Part 1 and Part 2',
        url: 'https://go.qwiklabs.com/arcade',
        time: '15 October 2022 - 30 June 2023',
        points: [
            "Fundamentals of the event was same as Before",
            "Arcade was game like program where we had to collect badges by completing labs within a given time, and each badge had it's own niche of Google Cloud Platform"
        ],
        id: 9
    },

]

function cardPosition(itemId: number) {
    return itemId % 2 === 0 ? 'cardPRight' : 'cardPLeft';
}

function timePosition(itemId: number) {
    return itemId % 2 === 0 ? 'timePLeft' : 'timePRight';
}
</script>
<template>
    <div>
        <div v-motion-slide-visible-bottom class="heading my-16">Experience</div>
        <div class="timeline-div">
            <div class="w-10 h-10  rounded-full translate-y-52 border-4 bg-[#17132b] border-[#17132b] p-1">
                <img loading="lazy" src="/images/experience/gc.svg" alt="Arcade">
            </div>
            <div class="w-10 h-10 rounded-full translate-y-[40rem] border-4 bg-[#17132b] border-[#17132b] p-1">
                <img loading="lazy" src="/images/experience/gc2.svg" alt="GoogleCloud">
            </div>
            <div class="w-10 h-10  rounded-full translate-y-[30rem] border-4 bg-[#17132b] border-[#17132b] p-1">
                <img loading="lazy" src="/images/experience/gc.svg" alt="Amazon ml">
            </div>
        </div>
        <div class="flex justify-center min-w-full" v-for="item in data" :key="item.id">
            <div v-motion-slide-visible-left :class="cardPosition(item.id)" class="flex justify-center w-full">
                <div $vanillaTilt data-tilt class="card card-color brdr">
                    <div class="inner blurblur">
                        <div class="text-2xl font-semibold mb-1 sm:text-3xl text-pink-400">{{ item.position }}</div>
                        <a :href="item.url" target="_blank" rel="noopener noreferrer"
                            class="text-xl sm:text-2xl font-normal underline underline-offset-2 text-blue-300">{{
                                item.company
                            }}</a>
                        <div :class="timePosition(item.id)"
                            class=" my-2 font-sans text-sm sm:text-base font-bold text-violet-400 pb-1">{{ item.time }}</div>
                        <ul class="text-sm sm:text-lg font-normal mb-1 list-disc list-inside" v-for="point in item.points"
                            :key="point">
                            <li class="py-1">{{ point }}</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<style scoped >
.card {
    @apply text-center block rounded-3xl text-white mt-4 h-auto w-11/12 md:w-1/2 lg:w-[36%] lg:m-4;
    transform-style: preserve-3d;
}
.inner{
    @apply w-full pt-6 md:p-2 lg:p-10;
}
.inner:hover {
    transform: translateZ(100px);
    transform: scale3d(50px);
}
.card img {
    width: 10px;
}

.timeline-div {
    @apply z-10 w-1 bg-[#17132b] sm:mx-auto sm:h-[57rem] lg:flex flex-col justify-start items-center mt-0 absolute left-1/2 transform -translate-x-1/2 hidden md:hidden;
}

.cardPRight {
    @apply sm:justify-end sm:pr-24;
}

.cardPLeft {
    @apply sm:justify-start sm:pl-24;
}

.timePLeft {
    @apply sm:transform md:-translate-x-0 lg:-translate-x-[31rem] lg:text-lg lg:translate-y-[5.2rem];
}

.timePRight {
    @apply sm:transform md:translate-x-0 lg:translate-x-[31rem] lg:translate-y-[2.8rem] sm:text-lg;
}</style>