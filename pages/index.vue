<template>
  <div class="notice-wrapper">
    <div class="notice-card">
      <img :src="imgLogo" alt="Firefly Logo" class="client-logo" />

      <span class="badge">Vaga Disponível</span>

      <h1>Firefly Client</h1>

      <div class="content-body">
        <p>
          Uma nova experiência para Minecraft, focada em
          <strong>performance extrema</strong>, visual moderno
          e estabilidade total.
        </p>

        <div class="banner-container">
          <img :src="imgVagas" alt="Recrutamento" class="promo-banner" />
        </div>

        <p>
          Desenvolvido com atenção aos mínimos detalhes,
          o Firefly Client entrega fluidez, segurança e um
          design elegante em cada atualização.
        </p>

        <div class="systems-container">
          <img :src="imgSistemas" alt="Sistemas Operacionais" class="systems-img" />
        </div>

        <p class="discord-info">
          Entre na nossa comunidade no Discord:
          <a href="https://discord.gg/firefly" target="_blank">Firefly Official</a>
        </p>
      </div>

      <button @click="handleDownload" class="download-button">
        BAIXAR FIREFLY.JAR
      </button>
    </div>
  </div>
</template>

<script setup>
/** * Como as imagens estão na raiz (onde está o package.json), 
 * usamos o caminho relativo './' para importá-las.
 */
import imgLogo from './dsd.png';
import imgVagas from './vagas_abertas.png';
import imgSistemas from './sistemas.png';

const handleDownload = () => {
  // Se o jar também estiver na raiz, ele precisará estar na pasta 'public'
  // para ser baixável diretamente, ou você deve importar o link dele aqui.
  const jarUrl = '/firefly-client.jar'; 
  const link = document.createElement('a');
  link.href = jarUrl;
  link.setAttribute('download', 'FireflyClient.jar');
  document.body.appendChild(link);
  link.click();
  document.body.removeChild(link);
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap');

.notice-wrapper {
  min-height: 100vh;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 2rem;
  font-family: 'Inter', sans-serif;
  background: 
    radial-gradient(circle at 80% 20%, rgba(93, 255, 179, 0.08), transparent 45%),
    linear-gradient(180deg, #07110b 0%, #020403 100%);
  color: #ecfff4;
}

.notice-card {
  width: min(580px, 100%);
  background: rgba(6, 20, 14, 0.8);
  border: 1px solid rgba(93, 255, 179, 0.18);
  border-radius: 28px;
  padding: 3.5rem 2.5rem;
  text-align: center;
  backdrop-filter: blur(25px) saturate(170%);
  -webkit-backdrop-filter: blur(25px) saturate(170%);
  box-shadow: 
    0 30px 60px rgba(0, 0, 0, 0.6),
    0 0 40px rgba(93, 255, 179, 0.15);
}

.client-logo {
  width: 80px;
  margin-bottom: 1rem;
  filter: drop-shadow(0 0 12px rgba(93, 255, 179, 0.4));
}

.badge {
  display: inline-block;
  padding: 0.4rem 1.1rem;
  border-radius: 50px;
  background: rgba(93, 255, 179, 0.12);
  border: 1px solid rgba(93, 255, 179, 0.45);
  font-size: 0.7rem;
  font-weight: 800;
  color: #5dffb3;
  text-transform: uppercase;
  letter-spacing: 0.08em;
  margin-bottom: 1.5rem;
  box-shadow: 0 0 15px rgba(93, 255, 179, 0.1);
}

h1 {
  font-size: 2.5rem;
  font-weight: 800;
  margin-bottom: 1.5rem;
  background: linear-gradient(180deg, #ffffff 0%, #a8e6c2 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.content-body p {
  color: #a8e6c2;
  line-height: 1.7;
  margin-bottom: 1.2rem;
}

strong {
  color: #5dffb3;
}

.promo-banner {
  width: 100%;
  border-radius: 14px;
  margin: 1rem 0;
  border: 1px solid rgba(255, 255, 255, 0.05);
}

.systems-img {
  width: 90%;
  max-width: 380px;
  margin: 1rem 0;
}

.download-button {
  margin-top: 1.5rem;
  width: 100%;
  padding: 1.2rem;
  background: #00ff95;
  color: #030a06;
  border: none;
  border-radius: 14px;
  font-size: 1.1rem;
  font-weight: 800;
  cursor: pointer;
  transition: all 0.3s ease;
  box-shadow: 0 0 20px rgba(0, 255, 149, 0.3);
  text-transform: uppercase;
}

.download-button:hover {
  transform: translateY(-3px);
  box-shadow: 0 0 40px rgba(0, 255, 149, 0.5);
  filter: brightness(1.1);
}

.discord-info {
  margin-top: 1rem;
  font-size: 0.9rem !important;
}

a {
  color: #5dffb3;
  text-decoration: none;
  font-weight: bold;
}
</style>