<template>
  <div class="main">
    <h2>Solução 1 - CssGrid</h2>
    <div class="cards var-grid">
      <div class="card" style="--grid-min: 150px">
        <div class="img"><div class="img__exemplo"></div></div>
        <div class="titulo">
          <h3>Titulo do card</h3>
        </div>
        <div class="conteudo">
          <p>Aqui temos um resumo do conteudo do assunto do card</p>
        </div>
      </div>
      <div class="card">
        <div class="img"><div class="img__exemplo"></div></div>
        <div class="titulo">
          <h3>Titulo do card 2</h3>
        </div>
        <div class="conteudo">
          <p>Aqui temos um resumo do conteudo do assunto do card</p>
        </div>
      </div>
      <div class="card">
        <div class="img"><div class="img__exemplo"></div></div>
        <div class="titulo">
          <h3>Titulo do card 2</h3>
        </div>
        <div class="conteudo">
          <p>Aqui temos um resumo do conteudo do assunto do card 3</p>
        </div>
      </div>
    </div>

    <h2>Solução 2 - FlexBox</h2>
    <div class="cards var-flex">
      <div class="card var-flex" style="--flex-min: 150px;">
        <div class="img"><div class="img__exemplo"></div></div>
        <div class="titulo">
          <h3>Titulo do card</h3>
        </div>
        <div class="conteudo">
          <p>Aqui temos um resumo do conteudo do assunto do card</p>
        </div>
      </div>
      <div class="card">
        <div class="img"><div class="img__exemplo"></div></div>
        <div class="titulo">
          <h3>Titulo do card 2</h3>
        </div>
        <div class="conteudo">
          <p>Aqui temos um resumo do conteudo do assunto do card</p>
        </div>
      </div>
      <div class="card">
        <div class="img"><div class="img__exemplo"></div></div>
        <div class="titulo">
          <h3>Titulo do card 2</h3>
        </div>
        <div class="conteudo">
          <p>Aqui temos um resumo do conteudo do assunto do card 3</p>
        </div>
      </div>
    </div>

    <h2>Solução 3 - FlexBox-2</h2>
    <div class="cards var-flex2">
      <div class="card var-flex2" style="--flex2-min: 150px;">
        <div class="img"><div class="img__exemplo"></div></div>
        <div class="titulo">
          <h3>Titulo do card</h3>
        </div>
        <div class="conteudo">
          <p>Aqui temos um resumo do conteudo do assunto do card</p>
        </div>
      </div>
      <div class="card var-flex2" style="--flex2-min: 80px;">
        <div class="img"><div class="img__exemplo"></div></div>
        <div class="titulo">
          <h3>Titulo do card 2</h3>
        </div>
        <div class="conteudo">
          <p>Aqui temos um resumo do conteudo do assunto do card</p>
        </div>
      </div>
      <div class="card var-flex2">
        <div class="img"><div class="img__exemplo"></div></div>
        <div class="titulo">
          <h3>Titulo do card 3</h3>
        </div>
        <div class="conteudo">
          <p>Aqui temos um resumo do conteudo do assunto do card 3</p>
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
:root {
  --grid-min: 300px;
  --flex-min: 300px;
  --flex2-min: 300px;
}

.main {
  grid-area: main;
  background: #f9f9f9;
  padding: 3rem 1rem;
}

.var-grid {
  display: grid;
  grid-gap: 1rem;
  grid-template-columns: repeat(auto-fit, minmax(var(--grid-min), 1fr));
}

.var-flex {
  display: flex;
  flex-wrap: wrap;
  margin: 1rem -0.5rem;

  > div {
    flex-grow: 1;
    flex-basis: calc((var(--flex-min) - 100%) * 999);
    margin: 0.5rem;

    &.flex--auto {
      flex: 0 1 auto;
    }
  	}
}

.var-flex2 {
  display: flex;
  flex-wrap: wrap;
  margin: 1rem -0.5rem;

  > * {
    flex: 1 1 var(--flex2-min);
    margin: 0.5rem;
    
    &.flex--auto {
      flex: 0 1 auto;
    }
  }
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
