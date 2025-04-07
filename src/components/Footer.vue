<template>
  <footer class="bg-gray-900 text-white py-12">
    <div class="container mx-auto px-4">
      <div class="text-center">
        <h3 class="text-2xl font-bold mb-4">Saiba ainda mais sobre mim.</h3>
        <div class="flex justify-center space-x-6 mb-8">
          <a href="https://wa.me/5511981927567" class="hover:text-green-500 transition-colors">
            <i class="fa-brands fa-whatsapp fa-2x"></i>
          </a>
          <a href="https://github.com/Lucas19Alves" class="hover:text-orange-500 transition-colors">
            <i class="fa-brands fa-github fa-2x"></i>
          </a>
          <a href="https://www.linkedin.com/in/lucaas19alves/" class="hover:text-blue-500 transition-colors">
            <i class="fa-brands fa-linkedin fa-2x"></i>
          </a>
        </div>
        <p class="text-gray-400">
          {{ new Date().getFullYear() }}, Lucas Alves.
        </p>
      </div>
    </div>
  </footer>
</template>

<!-- Importar FontAwesome -->
<style>
@import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css');
</style>