<script setup lang="ts">
import emailjs from '@emailjs/browser';
import { onMounted } from 'vue';

onMounted(() => {
  emailjs.init('cu17r5y9QKLHIvYoR');
});

const sendEmail = (event: Event) => {
  event.preventDefault();

  const form = event.target as HTMLFormElement;

  emailjs.sendForm('service_3g23jfi', 'template_y7ontwx', form)
    .then(() => {
      alert('Mensagem enviada com sucesso!');
      form.reset();
    })
    .catch((error) => {
      console.error('Erro ao enviar mensagem:', error);
      alert('Erro ao enviar a mensagem.');
    });
};
</script>


<template>
  <section id="contato" class="section-padding bg-gray-50 py-16">
    <div class="container mx-auto px-4">
      <!-- Título -->
      <h2 class="text-4xl font-bold text-center mb-12 text-gray-800" data-aos="fade-up">
        Entre em Contato
      </h2>

      <!-- Formulário -->
      <div class="max-w-2xl mx-auto">
        <form id="contactForm" @submit="sendEmail" class="space-y-6" data-aos="fade-up">
          <!-- Nome -->
          <div>
            <label for="name" class="block text-gray-700 font-medium mb-2">Nome</label>
            <input type="text" id="name" name="name" placeholder="Digite seu nome"
              class="w-full px-4 py-3 border border-gray-300 rounded-lg text-gray-700 focus:ring-2 focus:ring-blue-500 focus:border-transparent"
              required autocomplete="name">
          </div>

          <!-- Email -->
          <div>
            <label for="email" class="block text-gray-700 font-medium mb-2">E-mail</label>
            <input type="email" id="email" name="email" placeholder="Digite seu e-mail"
              class="w-full px-4 py-3 border border-gray-300 rounded-lg text-gray-700 focus:ring-2 focus:ring-blue-500 focus:border-transparent"
              required autocomplete="email">
          </div>

          <!-- Telefone -->
          <div>
            <label for="phone" class="block text-gray-700 font-medium mb-2">Telefone</label>
            <input type="tel" id="phone" name="phone" placeholder="Digite seu telefone"
              class="w-full px-4 py-3 border border-gray-300 rounded-lg text-gray-700 focus:ring-2 focus:ring-blue-500 focus:border-transparent"
              required autocomplete="tel">
          </div>

          <!-- Mensagem -->
          <div>
            <label for="message" class="block text-gray-700 font-medium mb-2">Mensagem</label>
            <textarea id="message" name="message" rows="5" placeholder="Digite sua mensagem"
              class="w-full px-4 py-3 border border-gray-300 rounded-lg text-gray-700 focus:ring-2 focus:ring-blue-500 focus:border-transparent"
              required></textarea>
          </div>

          <!-- Botão -->
          <button type="submit"
            class="w-full bg-primary hover:bg-secondary text-white font-semibold py-3 rounded-lg transition-all duration-300">
            Enviar Mensagem
          </button>
        </form>
      </div>
    </div>
  </section>
</template>



<style>
input,
textarea {
  transition: box-shadow 0.3s ease-in-out;
}

input:focus,
textarea:focus {
  box-shadow: 0 0 0 2px #3b82f6;
}
</style>
