<template >
    <section class="text-white mt-18" id="about">
        <div class="absolute z-0 top-[93rem] inset-x-0 h-64 flex items-start">
            <div class="h-24 w-64 bg-gradient-to-br from-primary via-secondary blur-2xl to-[#570cac] opacity-20"></div>
        </div>
        <div class="md:grid md:grid-cols-2 gap-8 items-center py-8 px-4 xl:gap-16 sm:py-16 xl:px-16 z-1">
            <div data-aos="flip-right">
                <h2 class="text-4xl font-bold text-white text-left mb-8">My Education</h2>
                <div class="space-y-8 py-8">
                    <div v-for="element in education" :key="element.id"
                    class="flex items-center md:w-[80%] w-full rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641]"
                    >
                        <div class="w-1/4">
                            <img src="https://img.icons8.com/ios-glyphs/60/ffffff/graduation-cap--v1.png" alt="graduation-cap--v1">
                        </div>
                        <div class="w-3/4 pl-4">
                            <h3 class="text-2xl font-semibold uppercase text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary lg:text-xl">
                                {{ element.School }}
                            </h3>
                            <p class="text-white">{{ element.program }}</p>
                            <p class="text-white">{{ element.mark }}</p>
                            <p class="text-white">{{ element.year }}</p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="mt-4 md:mt-0 text-left flex flex-col z-10 h-full" data-aos="flip-right">
                <h2 class="text-4xl font-bold text-white md:text-center text-left mb-4">More
                    <span class="text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary">About</span>
                    Me
                </h2>
                <p class="text-base lg:text-lg mt-8 py-8"> I’m an engineering graduate with a BTech in Aeronautical Engineering from KTU, and I’ve expanded my expertise through diplomas in Data Science and Programming from IIT Madras. My passion lies at the intersection of technology and problem-solving, where I enjoy building smart, scalable solutions that make an impact.

I’ve worked on diverse projects spanning machine learning, full-stack app development, and data analysis — experiences that have helped me blend analytical thinking with real-world application. From predictive modeling to crafting user-centric applications, I enjoy taking an idea from concept to execution.

I'm constantly learning, evolving, and exploring new technologies, with an aim to grow as a well-rounded developer and data enthusiast. I’m excited about future opportunities to collaborate, create, and contribute to meaningful innovations.
                </p>
                <div class="grid grid-cols-3 gap-4 max-w-lg pt-8">
                    
                    <div class="text-center rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641] p-3">
                        <h3 class="text-white font-bold text-xl sm:text-2xl lg:text-3xl">+4</h3>
                        <p class="text-sm sm:text-base text-gray-300">Project in Data Science and Programming</p>
                    </div>

                    <div class="text-center rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641] p-3">
                        <h3 class="text-white font-bold text-xl sm:text-2xl lg:text-3xl">+3</h3>
                        <p class="text-sm sm:text-base text-gray-300"> Years Experience in Teaching</p>
                    </div>

                    <div class="text-center rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641] p-3">
                        <h3 class="text-white font-bold text-xl sm:text-2xl lg:text-3xl">3 month</h3>
                        <p class="text-sm sm:text-base text-gray-300"> Internship as Junior Aeronautical Engineer</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
<script setup>
import { ref } from 'vue';
const education=ref([
    {
        id:1,
        School:'Indian Institute of technology, Madras, Tamil Nadu',
        program:'BS in Data science and Programming',
        mark:'CGPA: 9.6',
        year:'2022 - In Progress'
    },
    {
        id:2,
        School:'APJ Abdul Kalam Technological University, Kerala',
        program:'Bachelor of technology in Aeronautical Engineering',
        mark:'CGPA: 7.02',
        year:'2015 - 2019'
    },
    {
        id:3,
        School:'MES HSS Mannarkkad, Palakkad, Kerala',
        program:'Higher Secondary Education – Computer Science',
        mark:'Percentage: 88.6%',
        year:'2013 – 2015'
    }
])
</script>