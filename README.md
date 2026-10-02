# Cadastro de Produtos — MVC

Julia Da Silva Rodrigues Ferreira — RM 20240323 

como instalar e executar
npm install
npm start

Acesse http://localhost:3000 (redireciona para `/produtos`).
O arquivo `database.sqlite` é criado automaticamente na primeira execução.

estrutura (MVC)

- **Model:** `models/index.js` (`Produto`, `Categoria` e o relacionamento)
- **View:** `views/` (páginas EJS)
- **Controller:** `routes/produtos.js` e `routes/categorias.js`

 Funcionalidades

- Cadastro de produtos
- Listagem de produtos
- Edição de produtos
- Exclusão de produtos
- Cadastro de categorias
- Produto associado a uma categoria

Desafios

Desafio 1 — Categorias e relacionamento com produtos.
Criei o Model `Categoria` (`id`, `nome`) e o relacionamento 1:N com
`Categoria.hasMany(Produto)` e `Produto.belongsTo(Categoria)`. O Sequelize cria a chave
estrangeira `categoriaId` na tabela de produtos, então o vínculo fica gravado no banco.
A página `/categorias` permite cadastrar categorias; os formulários de produto têm um
`<select>` com as categorias; a listagem busca os produtos com `include` (JOIN) e exibe a
categoria de cada um.


# atividade-pw-3bim
