<script setup lang="ts">
const projetos = [
  
  {
    titulo: 'Dev Room',
    descricao: 'Plataforma de trabalho para desenvolvedores, com foco na concentração e gerenciamento de tarefas.',
    tecnologias: ['Vite', 'JavaScript', 'NodeJS', 'VueJS', 'TailwindCSS' , 'API'],
    imagem: new URL('../assets/devroom.png', import.meta.url).href,
    github: 'https://github.com/Lucas19Alves/dev-room',
    demo: 'https://dev-room-three.vercel.app/'
  },
  {
    titulo: 'Cardápio dígital',
    descricao: 'Cardápio de uma lanchonete com funcionalidades de horário de funcionamento e pedidos via WhatsApp.',
    tecnologias: ['JavaScript', 'TailwindCSS', 'API'],
    imagem: new URL('../assets/cardapio.png', import.meta.url).href,
    github: 'https://github.com/Lucas19Alves/cardapio',
    demo: 'https://cardapio-flax-five.vercel.app/'
  },
  {
    titulo: 'Gerador de Currículo',
    descricao: 'Gerador de currículo simples e prático, com opção de download em PDF.',
    tecnologias: ['JavaScript'],
    imagem: new URL('../assets/curriculo.png', import.meta.url).href,
    github: 'https://github.com/Lucas19Alves/gerador-curriculo',
    demo: 'https://gerador-curriculo-bice.vercel.app/'
  },
  {
    titulo: 'Sistema Hoteleiro (Em andamento)',
    descricao: 'Sistema de gerenciamento de reservas de um hotel, com opção de check-in e check-out.',
    tecnologias: ['JavaScript', 'NodeJS', 'PHP', 'MySQL', 'TailwindCSS' ],
    imagem: new URL('../assets/pms.png', import.meta.url).href,
    github: 'https://github.com/Lucas19Alves/PMS',
    demo: 'https://pms-gold.vercel.app/'
  },
  {
    titulo: 'Gerador de QRCode',
    descricao: 'Gerador de QRCode dinâmico com opção de download em PNG.',
    tecnologias: ['JavaScript', 'NodeJS', 'Express', 'VueJS', 'Bootstrap' , 'API'],
    imagem: new URL('../assets/qrcode.png', import.meta.url).href,
    github: 'https://github.com/Lucas19Alves/gerador-qr-code',
    demo: 'https://gerador-qr-code-plum.vercel.app/'
  },
  {
    titulo: 'Landing Page',
    descricao: 'Landing page de uma empresa de tecnologia, com animações e responsividade.',
    tecnologias: ['JavaScript', 'NodeJS', 'React', 'TailwindCSS' , 'API'],
    imagem: new URL('../assets/landing.png', import.meta.url).href,
    github: 'https://github.com/Lucas19Alves/sunshine-sol',
    demo: 'https://sunshine-sol-build.vercel.app/'
  },
  
];
</script>

<template>
  <section id="projetos" class="section-padding bg-gray-50">
    <div class="container mx-auto px-4">
      <!-- Título -->
      <h2 class="text-4xl font-bold text-center mb-12 text-gray-800" data-aos="fade-up">
        Projetos em Destaque
      </h2>
      
      <!-- Grid -->
      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
        <!-- Card do Projeto -->
        <div 
          v-for="(projeto, index) in projetos" 
          :key="projeto.titulo"
          class="bg-white rounded-lg shadow-lg overflow-hidden transform transition-all duration-300 hover:scale-105 hover:shadow-2xl"
          data-aos="fade-up"
          :data-aos-delay="index * 200"
        >
          <img :src="projeto.imagem" :alt="projeto.titulo" class="w-full h-48 object-cover">
          <div class="p-6">
            <h3 class="text-xl font-semibold mb-2 text-gray-800">{{ projeto.titulo }}</h3>
            <p class="text-gray-600 mb-4">{{ projeto.descricao }}</p>
            <div class="flex flex-wrap gap-2 mb-4">
              <span v-for="tech in projeto.tecnologias" 
                    :key="tech"
                    class="px-3 py-1 bg-blue-100 text-blue-800 rounded-full text-sm font-medium">
                {{ tech }}
              </span>
            </div>
            <!-- Botões -->
            <div class="flex space-x-4 mt-4">
              <a :href="projeto.github" 
                 target="_blank"
                 class="flex-1 text-center bg-primary text-white px-4 py-2 rounded-lg font-medium hover:bg-gray-600 transition">
                <i class="fas fa-code mr-2"></i> Ver Código
              </a>
              <a :href="projeto.demo" 
                 target="_blank"
                 class="flex-1 text-center bg-primary text-white px-4 py-2 rounded-lg font-medium hover:bg-blue-500 transition">
                <i class="fas fa-external-link-alt mr-2"></i> Ver Projeto
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<!-- Importar FontAwesome -->
<style>
@import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css');
</style>
