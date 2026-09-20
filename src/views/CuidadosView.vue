<script setup>
import { RouterLink } from 'vue-router'
import imagemCuidados from '../assets/images/cuidados.png'
</script>

<template>
  <main class="pagina">
    <section class="cabecalho-pagina">
      <div class="introducao">
        <span class="etiqueta">Adoção consciente</span>
        <h1>Cuidados antes da adoção</h1>
        <p>
          Adotar é assumir um compromisso de carinho e responsabilidade por toda a vida do animal.
          Antes de tomar essa decisão, confira se sua rotina e sua casa estão preparadas.
        </p>
      </div>

      <img :src="imagemCuidados" alt="Veterinária examinando um cão acompanhado por sua tutora" />
    </section>

    <section class="lista-cuidados">
      <div class="titulo-lista">
        <span>Checklist</span>
        <h2>O que você precisa considerar</h2>
      </div>

      <ul>
        <li>
          <span class="numero">01</span>
          <div>
            <h3>Alimentação adequada</h3>
            <p>Ofereça alimento de qualidade e na quantidade indicada para a idade e o porte.</p>
          </div>
        </li>
        <li>
          <span class="numero">02</span>
          <div>
            <h3>Espaço seguro</h3>
            <p>
              Prepare um ambiente protegido, confortável e compatível com as necessidades do animal.
            </p>
          </div>
        </li>
        <li>
          <span class="numero">03</span>
          <div>
            <h3>Vacinação em dia</h3>
            <p>Mantenha as vacinas e a vermifugação atualizadas para prevenir doenças.</p>
          </div>
        </li>
        <li>
          <span class="numero">04</span>
          <div>
            <h3>Higiene e bem-estar</h3>
            <p>Cuide da limpeza do ambiente, dos utensílios, do pelo, das unhas e dos dentes.</p>
          </div>
        </li>
        <li>
          <span class="numero">05</span>
          <div>
            <h3>Acompanhamento veterinário</h3>
            <p>
              Planeje consultas periódicas e tenha uma reserva para cuidados de saúde inesperados.
            </p>
          </div>
        </li>
      </ul>
    </section>

    <aside class="aviso">
      <div>
        <span aria-hidden="true">♡</span>
        <p>
          <strong>Lembre-se:</strong> tempo, paciência e afeto também fazem parte dos cuidados
          diários.
        </p>
      </div>
      <RouterLink class="botao-voltar" to="/animais">← Voltar aos animais</RouterLink>
    </aside>
  </main>
</template>

<style scoped>
.pagina {
  width: min(1040px, 92%);
  margin: 0 auto;
  padding: 64px 0 72px;
}

.cabecalho-pagina {
  display: grid;
  grid-template-columns: 0.9fr 1.1fr;
  align-items: center;
  gap: clamp(32px, 6vw, 70px);
}

.etiqueta,
.titulo-lista > span {
  display: inline-block;
  color: #176247;
  font-size: 13px;
  font-weight: 800;
  letter-spacing: 0.05em;
  text-transform: uppercase;
}

.etiqueta {
  padding: 7px 13px;
  background: #e4f2eb;
  border-radius: 999px;
}

.introducao h1 {
  margin: 16px 0 18px;
  color: #173c30;
  font-family: Georgia, 'Times New Roman', serif;
  font-size: clamp(40px, 6vw, 58px);
  line-height: 1.05;
}

.introducao p {
  margin: 0;
  color: #607169;
  font-size: 17px;
  line-height: 1.75;
}

.cabecalho-pagina img {
  width: 100%;
  height: 390px;
  object-fit: cover;
  border-radius: 24px;
  box-shadow: 0 20px 45px rgba(33, 66, 54, 0.15);
}

.lista-cuidados {
  display: grid;
  grid-template-columns: 0.65fr 1.35fr;
  gap: 55px;
  margin-top: 70px;
  padding: 42px;
  background: #eef6f1;
  border-radius: 24px;
}

.titulo-lista h2 {
  margin: 10px 0 0;
  color: #173c30;
  font-family: Georgia, 'Times New Roman', serif;
  font-size: 32px;
  line-height: 1.15;
}

.lista-cuidados ul {
  display: grid;
  gap: 12px;
  margin: 0;
  padding: 0;
  list-style: none;
}

.lista-cuidados li {
  display: flex;
  align-items: flex-start;
  gap: 17px;
  padding: 18px;
  background: white;
  border-radius: 14px;
}

.numero {
  display: grid;
  width: 38px;
  height: 38px;
  flex: 0 0 auto;
  place-items: center;
  color: white;
  background: #df754a;
  border-radius: 10px;
  font-size: 12px;
  font-weight: 850;
}

.lista-cuidados h3 {
  margin: 0 0 5px;
  color: #244b3d;
  font-size: 16px;
}

.lista-cuidados p {
  margin: 0;
  color: #6b7c74;
  font-size: 14px;
  line-height: 1.55;
}

.aviso {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 25px;
  margin-top: 28px;
  padding: 23px 28px;
  border: 1px solid #ead9c7;
  background: #fff8ed;
  border-radius: 18px;
}

.aviso > div {
  display: flex;
  align-items: center;
  gap: 12px;
}

.aviso > div > span {
  color: #cf633b;
  font-size: 27px;
}

.aviso p {
  margin: 0;
  color: #695a4e;
  line-height: 1.55;
}

.botao-voltar {
  flex: 0 0 auto;
  padding: 12px 16px;
  color: white;
  background: #1d5542;
  border-radius: 10px;
  font-size: 14px;
  font-weight: 800;
  text-decoration: none;
}

@media (max-width: 800px) {
  .cabecalho-pagina,
  .lista-cuidados {
    grid-template-columns: 1fr;
  }

  .cabecalho-pagina img {
    grid-row: 1;
    height: 300px;
  }

  .lista-cuidados {
    gap: 28px;
    padding: 26px;
  }

  .aviso {
    align-items: flex-start;
    flex-direction: column;
  }
}
</style>
