<template>
  <div class="main">
    <div class="cards">
      <div class="card">
        <div class="img"><div class="img__exemplo"></div></div>
        <div class="titulo">
          <h3>Titulo do card</h3>
        </div>
        <div class="conteudo">
          <p>Aqui temos um resumo do conteudo do assunto do card</p>
        </div>
      </div>
  </div>
  </div>
</template>

<script>
export default {
  name: "TelaPadrao",
};
</script>

<style lang="scss">
.main {
  grid-area: main;
  background: #f9f9f9;
  padding: 3rem 1rem;
}

.cards {
  padding: 1em;
  &.var-grid {
    border: 1px solid limegreen;
  }

  .card {
    border: 1px solid #dadce0;
    -moz-border-radius: 8px;
    border-radius: 8px;
    min-width: 20vh;
  }
}

.img {
  .img__exemplo {
    background-color: grey;
    width: 50px;
    height: 50px;
    margin: 0.5em;
  }
}
</style>
