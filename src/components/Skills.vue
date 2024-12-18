<script setup lang="ts">
const skills = {
  frontend: [
    { name: 'Vue.js', level: 95 },
    { name: 'React', level: 85 },
    { name: 'Angular', level: 85 },
    { name: 'JavaScript', level: 90 },
    { name: 'TypeScript', level: 80 },
    { name: 'Tailwind CSS', level: 100 },
  ],
  backend: [
    { name: 'Node.js', level: 90 },
    { name: 'Python', level: 80 },
    { name: 'MySQL', level: 85 },
    { name: 'MongoDB', level: 80 },
    { name: 'PHP', level: 85 },
  ],
  tools: [
    { name: 'Git', level: 95 },
    { name: 'Docker', level: 85 },
    { name: 'AWS', level: 80 },
    { name: 'CI/CD', level: 80 },
  ],
};
</script>

<template>
  <section id="skills" class="section-padding bg-gray-50">
    <div class="container mx-auto">
      <!-- Título -->
      <h2 
        class="text-4xl font-bold text-center mb-12 text-gray-800 hover:text-blue-500 transition-colors"
        data-aos="fade-up"
      >
        Habilidades
      </h2>
      
      <!-- Grid -->
      <div class="grid md:grid-cols-3 gap-8">
        <!-- Desenvolvimento Frontend -->
        <div 
          class="bg-white p-6 rounded-lg shadow-md" 
          data-aos="fade-up"
        >
          <h3 
            class="text-xl font-semibold mb-6 text-blue-600"
          >
            Desenvolvimento Frontend
          </h3>
          <div class="space-y-4">
            <div v-for="skill in skills.frontend" :key="skill.name">
              <div class="flex justify-between mb-1">
                <span class="text-gray-700">{{ skill.name }}</span>
                <span class="text-gray-500">{{ skill.level }}%</span>
              </div>
              <div class="w-full bg-gray-200 rounded-full h-2">
                <div 
                  class="bg-primary rounded-full h-2" 
                  :style="{ width: `${skill.level}%` }"
                ></div>
              </div>
            </div>
          </div>
        </div>

        <!-- Desenvolvimento backend -->
        <div 
          class="bg-white p-6 rounded-lg shadow-md" 
          data-aos="fade-up" 
          data-aos-delay="200"
        >
          <h3 
            class="text-xl font-semibold mb-6 text-green-600"
          >
          Desenvolvimento Backend
          </h3>
          <div class="space-y-4">
            <div v-for="skill in skills.backend" :key="skill.name">
              <div class="flex justify-between mb-1">
                <span class="text-gray-700">{{ skill.name }}</span>
                <span class="text-gray-500">{{ skill.level }}%</span>
              </div>
              <div class="w-full bg-gray-200 rounded-full h-2">
                <div 
                  class="bg-green-600 rounded-full h-2" 
                  :style="{ width: `${skill.level}%` }"
                ></div>
              </div>
            </div>
          </div>
        </div>

        <!-- Ferramentas e Tecnologias -->
        <div 
          class="bg-white p-6 rounded-lg shadow-md" 
          data-aos="fade-up" 
          data-aos-delay="400"
        >
          <h3 
            class="text-xl font-semibold mb-6 text-purple-600"
          >
            Ferramentas e Tecnologias
          </h3>
          <div class="space-y-4">
            <div v-for="skill in skills.tools" :key="skill.name">
              <div class="flex justify-between mb-1">
                <span class="text-gray-700">{{ skill.name }}</span>
                <span class="text-gray-500">{{ skill.level }}%</span>
              </div>
              <div class="w-full bg-gray-200 rounded-full h-2">
                <div 
                  class="bg-purple-600 rounded-full h-2" 
                  :style="{ width: `${skill.level}%` }"
                ></div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
