# ETAPA 1 — Definição do Tema e Funcionalidades Principais

```Tema do Aplicativo: BookHolder - Organizador de Leitura Pessoal```
>>Descrição:
>>O BookHolder é um aplicativo para gerenciamento de biblioteca pessoal, permitindo aos usuários catalogar livros, acompanhar progresso de leitura e explorar novos títulos através de integração com API pública.

```Funcionalidades Principais (Requisitos Funcionais)```
>>RF01: O usuário poderá buscar livros por título, autor ou ISBN na Google Books API.

>>RF02: O usuário poderá salvar livros em sua biblioteca pessoal com status (Quero Ler, Lendo, Lido).

>>RF03: O usuário poderá registrar e atualizar progresso de leitura (página atual/total).

>>RF04: O app exibirá estatísticas de leitura (livros lidos, tempo de leitura, etc.).

>>RF05: O app armazenará os dados da biblioteca pessoal localmente com Room Database.

```Operações de Rede```
>>O aplicativo buscará informações de livros na Google Books API via Retrofit para pesquisa e detalhes de livros.

>>As operações de criação, atualização e exclusão serão simuladas usando JSONPlaceholder para demonstração das requisições HTTP completas.

# ETAPA 2 - Definição do Fluxo de Navegação entre Activities ou Telas

```Diagrama Simples:```

<img width="643" height="138" alt="image" src="https://github.com/user-attachments/assets/4ca9aff8-c639-4d86-a809-fc7aaa0335bf" />


```Telas com Requisições Externas (Retrofit)```
>>SearchScreen - Busca livros na Google Books API (GET)

>>BookDetailScreen - Carrega detalhes da API (GET)

```Telas com Dados Locais (Room)```
>>LibraryScreen - Gerencia biblioteca pessoal (CRUD)

>>EditProgressScreen - Atualiza progresso (UPDATE)

>>StatsScreen - Exibe estatísticas (READ)


```Estratégia de Navegação:```
>>O app utilizará uma única Activity com Navigation Compose






