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

<img width="1612" height="1603" alt="deepseek_mermaid_20251030_2a5b94" src="https://github.com/user-attachments/assets/01baa45a-3532-413c-86a6-328c8179763f" />

```👤 Fluxo do Usuário no App:```

1. Início
SplashScreen: App inicia com tela de apresentação (2 segundos)

HomeScreen: Menu principal com 3 opções

2. Buscar Livros
SearchScreen: Usuário pesquisa livros na Google Books API

BookDetailScreen: Visualiza detalhes do livro selecionado

EditProgressScreen: Adiciona à biblioteca e define status/páginas

3. Minha Biblioteca
LibraryScreen: Visualiza todos os livros salvos (Quero Ler, Lendo, Lidos)

BookDetailScreen: Acessa detalhes de livro da biblioteca

EditProgressScreen: Atualiza progresso de leitura

4. Estatísticas
StatsScreen: Visualiza gráficos e métricas de leitura

Dados calculados automaticamente da biblioteca pessoal

```Navegação Circular:```

O usuário pode navegar livremente entre as funcionalidades, criando um fluxo contínuo de descoberta e organização de leitura.

#ETAPA 3 - Planejamento do Banco de Dados (Room)

```Entidade: Book:```

<img width="590" height="296" alt="image" src="https://github.com/user-attachments/assets/30ca723c-783f-4355-ac1d-df602c44685e" />


```Entidade: UserBook:```

<img width="625" height="303" alt="image" src="https://github.com/user-attachments/assets/8e019c92-218e-47fa-a005-8496e99486ac" />


```Entidade: ReadingSession:```

<img width="595" height="203" alt="image" src="https://github.com/user-attachments/assets/9605a5db-337b-41af-9804-d0d61f3d6cc6" />

```Diagrama de Banco de Dados:```

<img width="546" height="174" alt="image" src="https://github.com/user-attachments/assets/6615df9d-9a6d-4b43-a689-ca129bbc8445" />


```Como os Dados Serão Persistidos:```

```Localmente (Room):```

>>Todos os dados da biblioteca pessoal ficam salvos no celular

>>Funciona offline sem internet

```Na Nuvem (APIs):```

>>Busca de livros → Google Books API

>>Operações de salvar/editar → JSONPlaceholder (simulação)







