<template>
    <section class="bg-gray-300 min-h-screen flex items-center justify-center py-16">
        <div class="max-w-7xl mx-auto text-center px-4 sm:px-6 lg:px-8">
            <h2 class="text-3xl md:text-4xl font-bold text-gray-800 mb-12 md:mb-32">
                How GO PLATFORM Can Help You?
            </h2>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8 px-4">
                <div 
                    v-for="(card, index) in cards" 
                    :key="index"
                    class="bg-gradient-to-r from-[#09ADFF] to-[#44C6C6] text-white p-8 rounded-2xl shadow-lg text-left
                           transform transition duration-300 hover:scale-105 hover:shadow-xl cursor-pointer">
                    <h3 class="text-xl md:text-2xl font-semibold mb-6 text-center">{{ card.title }}</h3>
                    <ul class="list-disc list-outside space-y-3 text-base md:text-lg">
                        <li v-for="(point, i) in card.points" :key="i" class="leading-relaxed">
                            {{ point }}
                        </li>
                    </ul>
                </div>
            </div>
            <button
                class="mt-12 md:mt-32 bg-yellow-500 text-white font-semibold py-4 px-8 rounded-full shadow-lg
                       hover:bg-yellow-600 hover:shadow-xl transition duration-300">
                More about Go Platform
            </button>
        </div>
    </section>
</template>


<script setup>

const cards = [
    {
        title: "Mobilize Your Workforce",
        points: [
            "Identify and unlock hidden potential within your team",
            "Prepare employees for critical roles with tailored guidance",
            "Use adaptable tools to help your workforce thrive in any industry",
        ],
    },
    {
        title: "Empower Continuous Skill Development",
        points: [
            "Provide personalized training programs to bridge skill gaps",
            "Connect learning outcomes with measurable business success",
            "Foster a culture of growth, innovation, and adaptability",
        ],
    },
    {
        title: "Build a Stronger Future with Smarter Hiring",
        points: [
            "Leverage skill-based assessments to find the right talent",
            "Streamline hiring decisions with unbiased and efficient tools",
            "Align new hires with your business goals for lasting success",
        ],
    },
]
</script>

