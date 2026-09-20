<script setup>
import { RouterLink } from 'vue-router'
import imagemCachorro from '../assets/images/cachorro.png'
import imagemGato from '../assets/images/gato.png'
import imagemGato2 from '../assets/images/gato2.png'
</script>

<template>
  <main class="pagina">
    <header class="titulo">
      <span class="etiqueta">Esperando por você</span>
      <h1>Animais disponíveis</h1>
      <p>Conheça três amigos cheios de personalidade e prontos para fazer parte de uma família.</p>
    </header>

    <section class="cards" aria-label="Animais disponíveis para adoção">
      <article class="card">
        <div class="foto">
          <img :src="imagemCachorro" alt="Bento, cão caramelo disponível para adoção" />
          <span class="destaque">Porte médio</span>
        </div>
        <div class="conteudo">
          <div class="identificacao">
            <h2>Bento</h2>
            <span>3 anos</span>
          </div>
          <p>
            Bento é brincalhão, companheiro e adora passeios ao ar livre. Ele se dá bem com crianças
            e está sempre pronto para aprender um truque novo.
          </p>
          <strong class="comportamento">Sociável e cheio de energia</strong>
        </div>
      </article>

      <article class="card">
        <div class="foto">
          <img :src="imagemGato" alt="Lua, gata preta e branca disponível para adoção" />
          <span class="destaque">Porte pequeno</span>
        </div>
        <div class="conteudo">
          <div class="identificacao">
            <h2>Lua</h2>
            <span>2 anos</span>
          </div>
          <p>
            Lua é uma gatinha tranquila e carinhosa. Gosta de lugares aconchegantes, de observar a
            janela e de receber carinho quando se sente segura.
          </p>
          <strong class="comportamento">Calma e muito afetuosa</strong>
        </div>
      </article>

      <article class="card">
        <div class="foto">
          <img :src="imagemGato2" alt="Amora, gata cinza rajada disponível para adoção" />
          <span class="destaque">Porte pequeno</span>
        </div>
        <div class="conteudo">
          <div class="identificacao">
            <h2>Amora</h2>
            <span>1 ano</span>
          </div>
          <p>
            Amora é curiosa, divertida e gosta de acompanhar tudo o que acontece ao seu redor. Ela
            adora brinquedos, cantinhos ensolarados e a companhia de pessoas tranquilas.
          </p>
          <strong class="comportamento">Curiosa e brincalhona</strong>
        </div>
      </article>
    </section>

    <aside class="chamada">
      <div>
        <span>Antes de decidir</span>
        <h2>Prepare-se para receber seu novo amigo</h2>
      </div>
      <RouterLink to="/cuidados">Ver cuidados essenciais →</RouterLink>
    </aside>
  </main>
</template>

<style scoped>
.pagina {
  width: min(1120px, 92%);
  margin: 0 auto;
  padding: 64px 0 72px;
}

.titulo {
  max-width: 680px;
  margin: 0 auto 40px;
  text-align: center;
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

.titulo h1 {
  margin: 14px 0 12px;
  color: #173c30;
  font-family: Georgia, 'Times New Roman', serif;
  font-size: clamp(38px, 6vw, 54px);
}

.titulo p {
  margin: 0;
  color: #687970;
  font-size: 17px;
  line-height: 1.7;
}

.cards {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 28px;
}

.card {
  overflow: hidden;
  border: 1px solid #e1e8e4;
  background: white;
  border-radius: 22px;
  box-shadow: 0 14px 36px rgba(33, 66, 54, 0.1);
  transition:
    transform 0.25s ease,
    box-shadow 0.25s ease;
}

.card:hover {
  box-shadow: 0 20px 42px rgba(33, 66, 54, 0.16);
  transform: translateY(-5px);
}

.foto {
  position: relative;
}

.foto img {
  width: 100%;
  height: 330px;
  object-fit: cover;
}

.destaque {
  position: absolute;
  right: 18px;
  bottom: 18px;
  padding: 8px 12px;
  color: #173c30;
  background: rgba(255, 255, 255, 0.94);
  border-radius: 999px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  font-size: 13px;
  font-weight: 800;
}

.conteudo {
  padding: 25px;
}

.identificacao {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 15px;
}

.identificacao h2 {
  margin: 0;
  color: #194f3d;
  font-family: Georgia, 'Times New Roman', serif;
  font-size: 32px;
}

.identificacao span {
  color: #bd5934;
  font-weight: 800;
}

.conteudo p {
  min-height: 100px;
  margin: 15px 0 18px;
  color: #607169;
  line-height: 1.65;
}

.comportamento {
  display: inline-flex;
  align-items: center;
  gap: 7px;
  color: #176247;
  font-size: 14px;
}

.comportamento::before {
  content: '●';
  font-size: 9px;
}

.chamada {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 30px;
  margin-top: 36px;
  padding: 27px 30px;
  color: white;
  background: #1d5542;
  border-radius: 20px;
}

.chamada span {
  color: #bbddcf;
  font-size: 12px;
  font-weight: 800;
  letter-spacing: 0.08em;
  text-transform: uppercase;
}

.chamada h2 {
  margin: 5px 0 0;
  font-family: Georgia, 'Times New Roman', serif;
  font-size: 23px;
}

.chamada a {
  flex: 0 0 auto;
  padding: 12px 16px;
  color: #173c30;
  background: #fff;
  border-radius: 10px;
  font-size: 14px;
  font-weight: 800;
  text-decoration: none;
}

@media (max-width: 900px) {
  .cards {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 650px) {
  .cards {
    grid-template-columns: 1fr;
  }

  .conteudo p {
    min-height: auto;
  }

  .chamada {
    align-items: flex-start;
    flex-direction: column;
  }
}
</style>
