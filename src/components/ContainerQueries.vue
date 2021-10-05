<template>
  <div class="main">
    <section class="section">
      <h1>Container Queries</h1>
      <h3>"Agora não dá, na volta a gente compra" - Será?</h3>
      <h4>Porque esse hype todo?</h4>
      <p>
        <a
          href="https://ishadeed.com/article/say-hello-to-css-container-queries/"
          >Sobre Container Queries</a
        >
      </p>
    </section>
    <section class="section">
      <ul>
        <h4>
          Container Queries virão para revolucionar o jeito de fazer interfaces
          responsivas(?)
        </h4>
        <li class="item">
          Podemos definir as caracateristícas de um elemento filho de acordo com
          o tamanho do elemento pai
          <div>
            <h5>Veja só essa aplicação</h5>
            <img
              src="https://ishadeed.com/assets/cq/intro.jpg"
              class="img__exemplo"
              aria="Qual a diferença?"
            />
            <h6>
              Basicamente, antes um media query era determinado pelo tamanho da
              View Port. Agora isso não precisa se reestringir somente a isso.
            </h6>
          </div>
        </li>
        <li class="item">
          Você pode ter o seu "próprio bootstrap" só que melhor!
          <div>
            <h5></h5>
            <img
              src="../assets/codigo1.png"
              class="img__exemplo"
              aria="Setup Simples"
            />
            <h4>
              Uma vez que temos a definição de tamanho do pai do elemento, temos
              uma contextualização de componente muito melhor
            </h4>
          </div>
        </li>
        <li class="item">
          <div>
            <h2>Houston We have a problem:</h2>
            <h5>Vamos olhas o Can I Use?</h5>
            <a href="https://caniuse.com/css-container-queries"
              >Can I Use /?css="Container Queries"?</a
            >
            <h6>Triste, complicado... Como tudo em CSS, como na vida</h6>
          </div>
        </li>
        <li class="item">
          <div>
            <h5>
              Ok... É triste mesmo, e também muito Legal. Mas se não funciona em
              nada ainda, porque você ta mostrando isso?
            </h5>
            <h2>
              Porque é <strong>possível</strong> fazer coisas parecidas e usar
              como <strong>Fallback no futuro</strong>
            </h2>
          </div>
        </li>
      </ul>
    </section>
    <section class="section">
      <h2>Direto ao assunto</h2>
      <div style="margin: 2em 0">
        <TelaPadrao />
      </div>
    </section>
  </div>
</template>

<script>
import TelaPadrao from "./TelaPadrao.vue";

export default {
  name: "ContainerQueries",
  components: {
    TelaPadrao,
  },
};
</script>
<style scoped lang="scss">
.section {
  display: flex;
  flex: 0 0 100%;
  justify-items: center;
  flex-direction: column;
  background: #ffffff;
  border: 1px solid #dadce0;
  -moz-border-radius: 8px;
  border-radius: 8px;
  position: relative;
  margin: 1em 0 1em 1em;
  padding: 1em;

  .item {
    width: 100%;
  }
  .img__exemplo,
  .img__prototipo {
    max-width: 50%;
  }
}
h3 {
  margin: 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
a {
  color: #42b983;
}
</style>
