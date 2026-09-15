# Pokedex - API de Pokémon

### 1. Qual API você usou
Foi utilizada a **PokéAPI** (Documentação: [https://pokeapi.co/docs/v2](https://pokeapi.co/docs/v2)).

### 2. O que ela devolve
A API devolve dados detalhados do Pokémon buscado (como altura, peso, experiência base, tipos e sprites), além do endpoint de espécie e da cadeia de evolução (*evolution chain*).

### 3. O endereço que você chamou
URL completa de consulta para o Pokémon Pikachu:
`https://pokeapi.co/api/v2/pokemon/pikachu`

### 4. Como rodar
Basta abrir o arquivo `index.html` diretamente em qualquer navegador web, sem a necessidade de rodar um servidor local.

### 5. Um print da tela funcionando!
[Tela Funcionando](./funcionando.png)
[Tela Json puro](./Json.png)

### 6. Uma dificuldade que você teve
Para exibir a linha evolutiva completa, a PokéAPI não retorna os dados diretamente na primeira busca. Foi necessário encadear três requisições (`fetch` do Pokémon -> `fetch` da espécie -> `fetch` da cadeia evolutiva) e usar `Promise.all` para buscar as imagens e dados de cada evolução separadamente.
