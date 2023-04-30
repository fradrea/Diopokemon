# Diopokemon
<!DOCTYPE html>
<html lang="pt-BR">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Pokédex</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <header>
      <h1>Pokédex</h1>
      <div class="search">
        <input type="text" id="searchInput" placeholder="Buscar Pokemon por nome, número ou tipo"/>
        <button id="searchButton">Pesquisar</button>
      </div>
    </header>
    <main>
      <ul id="pokemonList" class="pokemons"></ul>
      <div id="loadMore">
        <button id="loadMoreButton">Carregar mais</button>
      </div>
      <button id="backToTopButton" class="backToTopButton">Voltar ao topo</button>
    </main>
    <footer>
      <p>Desenvolvido por [seu nome]</p>
    </footer>
    <script src="script.js"></script>
  </body>
</html>
CSS:

css
Copy code
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  font-family: "Helvetica Neue", sans-serif;
}

header {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 1rem;
  background-color: #f7dfb9;
}

h1 {
  margin: 0;
  font-size: 2rem;
  color: #af2f2f;
}

.search {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  margin-top: 1rem;
}

.search input[type="text"] {
  padding: 0.5rem;
  font-size: 1rem;
  border-radius: 1rem 0 0 1rem;
  border: none;
  width: 60%;
}

.search button {
  padding: 0.5rem;
  font-size: 1rem;
  border-radius: 0 1rem 1rem 0;
  border: none;
  background-color: #a97e3f;
  color: #fff;
}

.backToTopButton {
  display: none;
  position: fixed;
  bottom: 20px;
  right: 30px;
  z-index: 99;
  font-size: 1rem;
  border: none;
  outline: none;
  background-color: #a97e3f;
  color: white;
  cursor: pointer;
  padding: 1rem;
  border-radius: 50%;
}

.backToTopButton:hover {
  background-color: #777;
}

main {
  display: flex;
  flex-direction: column;
  align-items: center;
  min-height: 100vh;
  background-color: #fff;
  padding: 1rem;
}

.pokemons {
  display: grid;
  grid-template-columns: 1fr;
  grid-gap: 1rem;
  width: 100%;
  max-width: 500px;
  margin-bottom: 2rem;
}

.pokemon {
  display: flex;
  flex-direction: column;
  margin: 0.5rem;
  padding: 1rem;
  border-radius: 1rem;
  background-color: #49d0b
