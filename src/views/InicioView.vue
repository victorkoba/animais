<script setup>
import { RouterLink } from 'vue-router'
import imagemCapa from '../assets/images/capa-adocao.png'
</script>

<template>
  <main>
    <section class="apresentacao">
      <div class="texto">
        <span class="etiqueta">Adoção responsável</span>
        <h1>Patas do Vale</h1>

        <p class="descricao">
          O Patas do Vale é uma organização fictícia criada para aproximar animais que esperam por
          um lar de pessoas dispostas a oferecer carinho, segurança e cuidado. Nosso portal divulga
          histórias de cães e gatos disponíveis para adoção e compartilha orientações essenciais
          para que cada encontro se transforme em uma amizade para toda a vida.
        </p>

        <p class="convite">Conheça nossos animais e encontre um novo companheiro!</p>

        <RouterLink class="botao" to="/animais">
          Ver animais disponíveis
          <span aria-hidden="true">→</span>
        </RouterLink>
      </div>

      <figure class="imagem-capa">
        <img :src="imagemCapa" alt="Cão e gato juntos no jardim de um abrigo" />
        <figcaption>Todo animal merece a chance de recomeçar.</figcaption>
      </figure>
    </section>

    <section class="valores" aria-label="Valores do Patas do Vale">
      <article>
        <span aria-hidden="true">♡</span>
        <div>
          <h2>Acolher</h2>
          <p>Cada história é recebida com respeito e carinho.</p>
        </div>
      </article>
      <article>
        <span aria-hidden="true">⌂</span>
        <div>
          <h2>Conectar</h2>
          <p>Ajudamos famílias e animais a se encontrarem.</p>
        </div>
      </article>
      <article>
        <span aria-hidden="true">✓</span>
        <div>
          <h2>Orientar</h2>
          <p>Incentivamos escolhas conscientes e responsáveis.</p>
        </div>
      </article>
    </section>
  </main>
</template>

<style scoped>
main {
  overflow: hidden;
}

.apresentacao {
  display: grid;
  width: min(1120px, 92%);
  grid-template-columns: 0.9fr 1.1fr;
  align-items: center;
  gap: clamp(36px, 6vw, 80px);
  margin: 0 auto;
  padding: 72px 0 54px;
}

.etiqueta {
  display: inline-block;
  padding: 7px 13px;
  color: #176247;
  background: #e4f2eb;
  border-radius: 999px;
  font-size: 13px;
  font-weight: 800;
  letter-spacing: 0.04em;
  text-transform: uppercase;
}

h1 {
  max-width: 520px;
  margin: 18px 0 20px;
  color: #173c30;
  font-family: Georgia, 'Times New Roman', serif;
  font-size: clamp(48px, 7vw, 76px);
  line-height: 0.98;
}

.descricao {
  max-width: 590px;
  margin: 0;
  color: #526159;
  font-size: 17px;
  line-height: 1.8;
}

.convite {
  margin: 22px 0;
  color: #2f4c41;
  font-size: 18px;
  font-weight: 750;
}

.botao {
  display: inline-flex;
  align-items: center;
  gap: 12px;
  padding: 14px 20px;
  color: white;
  background: #df754a;
  border-radius: 12px;
  box-shadow: 0 10px 24px rgba(199, 91, 48, 0.24);
  font-weight: 800;
  text-decoration: none;
  transition:
    transform 0.2s ease,
    background 0.2s ease;
}

.botao:hover {
  background: #c96039;
  transform: translateY(-2px);
}

.imagem-capa {
  position: relative;
  margin: 0;
}

.imagem-capa::before {
  position: absolute;
  z-index: -1;
  inset: -24px 32px 24px -24px;
  background: #e4f2eb;
  border-radius: 34px;
  content: '';
}

.imagem-capa img {
  width: 100%;
  aspect-ratio: 4 / 3;
  object-fit: cover;
  border-radius: 28px;
  box-shadow: 0 24px 55px rgba(27, 66, 52, 0.18);
}

.imagem-capa figcaption {
  position: absolute;
  right: 18px;
  bottom: 18px;
  max-width: 250px;
  padding: 12px 16px;
  color: #173c30;
  background: rgba(255, 255, 255, 0.92);
  border-radius: 12px;
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.12);
  font-size: 14px;
  font-weight: 750;
}

.valores {
  display: grid;
  width: min(1120px, 92%);
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
  margin: 0 auto 72px;
}

.valores article {
  display: flex;
  align-items: flex-start;
  gap: 15px;
  padding: 22px;
  border: 1px solid #e4e8e5;
  background: white;
  border-radius: 16px;
}

.valores article > span {
  display: grid;
  width: 38px;
  height: 38px;
  flex: 0 0 auto;
  place-items: center;
  color: #176247;
  background: #e4f2eb;
  border-radius: 50%;
  font-size: 21px;
  font-weight: 800;
}

.valores h2 {
  margin: 0 0 5px;
  color: #244b3d;
  font-size: 17px;
}

.valores p {
  margin: 0;
  color: #6b7c74;
  font-size: 14px;
  line-height: 1.5;
}

@media (max-width: 850px) {
  .apresentacao {
    grid-template-columns: 1fr;
    padding-top: 48px;
  }

  .imagem-capa {
    grid-row: 1;
  }

  .valores {
    grid-template-columns: 1fr;
  }
}
</style>
