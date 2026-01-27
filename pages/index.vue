<template>
  <div class="notice-wrapper">
    <div class="notice-card">
      <div class="logo-container">
        <img :src="imgLogo" alt="Firefly Logo" class="client-logo" />
      </div>

      <div class="badge-container">
        <span class="badge">Vaga Disponível</span>
      </div>

      <h1>Firefly Client</h1>

      <div class="content-body">
        <p class="intro-text">
          Uma nova experiência para Minecraft, focada em 
          <span class="highlight">performance extrema</span>, 
          visual moderno e estabilidade total.
        </p>

        <div class="banner-container">
          <img :src="imgVagas" alt="Estamos Recrutando" class="promo-banner" />
        </div>

        <p class="footer-text">
          Desenvolvido com atenção aos mínimos detalhes, o Firefly Client 
          entrega fluidez, segurança e um design elegante em cada atualização.
        </p>

        <div class="systems-container">
          <img :src="imgSistemas" alt="OS Support" class="systems-img" />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
// Importando direto da base (raiz do projeto)
import imgLogo from './dsd.png';
import imgVagas from './vagas_abertas.png';
import imgSistemas from './sistemas.png';
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;800&display=swap');

.notice-wrapper {
  min-height: 100vh;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 40px 20px;
  font-family: 'Inter', sans-serif;
  background-color: #020403;
  color: #ecfff4;
}

.notice-card {
  width: 100%;
  max-width: 540px;
  background: rgba(7, 17, 11, 0.45);
  border: 1px solid rgba(93, 255, 179, 0.15);
  border-radius: 32px;
  padding: 4rem 2.5rem;
  text-align: center;
  backdrop-filter: blur(20px);
  -webkit-backdrop-filter: blur(20px);
  box-shadow: 0 0 80px rgba(0, 0, 0, 0.6);
}

/* --- EFEITOS NAS IMAGENS --- */

/* 1. Logo: Aumenta o brilho e cresce levemente */
.client-logo {
  width: 100px;
  filter: drop-shadow(0 0 10px rgba(0, 255, 149, 0.4));
  transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
  cursor: pointer;
}

.client-logo:hover {
  transform: scale(1.1) rotate(5deg);
  filter: drop-shadow(0 0 25px rgba(0, 255, 149, 0.8));
}

/* 2. Banner: Efeito de "Lift" e claridade */
.promo-banner {
  width: 100%;
  border-radius: 18px;
  border: 1px solid rgba(255, 255, 255, 0.05);
  transition: all 0.5s ease;
  cursor: pointer;
}

.promo-banner:hover {
  transform: translateY(-10px) scale(1.02);
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.4), 0 0 20px rgba(0, 255, 149, 0.1);
  filter: brightness(1.1);
}

/* 3. Sistemas: Flutuação suave */
.systems-img {
  max-width: 280px;
  width: 70%;
  transition: all 0.4s ease;
  opacity: 0.7;
}

.systems-img:hover {
  opacity: 1;
  transform: scale(1.05);
  filter: drop-shadow(0 0 15px rgba(255, 255, 255, 0.2));
}

/* --- ESTILIZAÇÃO GERAL --- */

.logo-container { margin-bottom: 1rem; }
.badge-container { margin-bottom: 1.5rem; }

.badge {
  display: inline-block;
  padding: 6px 16px;
  border-radius: 50px;
  border: 1px solid rgba(0, 255, 149, 0.4);
  background: rgba(0, 255, 149, 0.05);
  font-size: 11px;
  font-weight: 800;
  color: #5dffb3;
  text-transform: uppercase;
}

h1 {
  font-size: 2.8rem;
  font-weight: 800;
  margin-bottom: 2rem;
  color: #ffffff;
}

.highlight {
  color: #00ff95;
  font-weight: 700;
}

.banner-container { margin-bottom: 2.5rem; }

.footer-text {
  color: #a8e6c2;
  font-size: 0.95rem;
  margin-bottom: 2rem;
}
</style>