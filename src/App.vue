<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <div class="aplicacao">
    <header class="cabecalho">
      <div class="cabecalho-conteudo">
        <RouterLink class="marca" to="/" aria-label="Ir para o início">
          <span class="marca-icone" aria-hidden="true">🐾</span>
          <span>
            <strong>Patas do Vale</strong>
            <small>Portal de adoção responsável</small>
          </span>
        </RouterLink>

        <nav class="menu" aria-label="Navegação principal">
          <RouterLink to="/">Início</RouterLink>
          <RouterLink to="/animais">Animais</RouterLink>
          <RouterLink to="/cuidados">Cuidados</RouterLink>
        </nav>
      </div>
    </header>

    <div class="conteudo-principal">
      <RouterView />
    </div>

    <footer class="rodape">
      <p>
        Projeto desenvolvido por
        <strong>Enrico Naba Augusto, Rodrigo Santos Graça e Victor Luiz Koba Batista</strong>
      </p>
      <p>Feito com carinho por quem acredita em novos começos.</p>
    </footer>
  </div>
</template>

<style>
:root {
  color: #23362f;
  background: #fbfaf7;
  font-family:
    Inter,
    ui-sans-serif,
    system-ui,
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    sans-serif;
  font-synthesis: none;
  text-rendering: optimizeLegibility;
}

* {
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  min-width: 320px;
  min-height: 100vh;
  margin: 0;
}

body,
button,
a {
  font-family: inherit;
}

a {
  color: inherit;
}

img {
  display: block;
  max-width: 100%;
}

.aplicacao {
  display: flex;
  min-height: 100vh;
  flex-direction: column;
}

.cabecalho {
  position: sticky;
  z-index: 10;
  top: 0;
  border-bottom: 1px solid rgba(31, 111, 84, 0.12);
  background: rgba(255, 255, 255, 0.94);
  backdrop-filter: blur(12px);
}

.cabecalho-conteudo {
  display: flex;
  width: min(1120px, 92%);
  min-height: 78px;
  align-items: center;
  justify-content: space-between;
  gap: 32px;
  margin: 0 auto;
}

.marca {
  display: flex;
  align-items: center;
  gap: 12px;
  color: #194f3d;
  text-decoration: none;
}

.marca-icone {
  display: grid;
  width: 44px;
  height: 44px;
  place-items: center;
  background: #e4f2eb;
  border-radius: 14px;
  font-size: 23px;
}

.marca strong,
.marca small {
  display: block;
}

.marca strong {
  font-family: Georgia, 'Times New Roman', serif;
  font-size: 22px;
}

.marca small {
  margin-top: 2px;
  color: #6b7c74;
  font-size: 12px;
}

.menu {
  display: flex;
  align-items: center;
  gap: 8px;
}

.menu a {
  padding: 10px 15px;
  border-radius: 999px;
  color: #4a5f56;
  font-size: 15px;
  font-weight: 700;
  text-decoration: none;
  transition:
    background 0.2s ease,
    color 0.2s ease;
}

.menu a:hover,
.menu a.router-link-active {
  color: #176247;
  background: #e4f2eb;
}

.conteudo-principal {
  flex: 1;
}

.rodape {
  display: flex;
  justify-content: space-between;
  gap: 24px;
  padding: 28px max(4%, calc((100% - 1120px) / 2));
  color: #dce9e4;
  background: #173c30;
  font-size: 13px;
  line-height: 1.6;
}

.rodape p {
  margin: 0;
}

@media (max-width: 700px) {
  .cabecalho-conteudo {
    min-height: auto;
    flex-direction: column;
    gap: 14px;
    padding: 16px 0 12px;
  }

  .menu {
    width: 100%;
    justify-content: center;
  }

  .menu a {
    padding: 8px 12px;
  }

  .rodape {
    flex-direction: column;
    text-align: center;
  }
}
</style>
