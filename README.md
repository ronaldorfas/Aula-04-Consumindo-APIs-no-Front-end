# 📚 Aula 04 — Consumindo APIs no Front-end

> Material organizado a partir da aula **“Consumindo APIs no Front-end”**, de Prof. Me. Deivison S. Takatu.

---

## 🧭 Índice

- [🔌 API — Application Programming Interface](#-api--application-programming-interface)
- [🌐 REST](#-rest)
- [📡 Protocolo HTTP](#-protocolo-http)
- [🛣️ Métodos HTTP](#️-métodos-http)
- [🎯 Endpoint](#-endpoint)
- [🗂️ APIs Públicas](#️-apis-públicas)
- [📦 JSON](#-json)
- [🔄 Como funciona uma requisição](#-como-funciona-uma-requisição)
- [🖥️ Backend e Web Service](#️-backend-e-web-service)
- [🚀 Express.js](#-expressjs)
- [☁️ Render](#️-render)
- [📝 Atividade 01](#-atividade-01)
- [📝 Atividade 02](#-atividade-02)
- [🔗 Links dos projetos](#-links-dos-projetos)

---

## 🔌 API — Application Programming Interface

Uma **API (Application Programming Interface)** é um conjunto de protocolos, rotinas e ferramentas para construção de software.

Ela define como diferentes componentes de software devem interagir, permitindo que sistemas distintos se comuniquem entre si.

---

## 🌐 REST

**REST (Representational State Transfer)** é um estilo arquitetural para desenvolvimento de sistemas distribuídos, especialmente aplicado à Web.

Principais princípios apresentados na aula:

- 🔹 Comunicação cliente-servidor sem estado (**stateless**)
- 🔹 Uso padrão dos métodos HTTP
- 🔹 Recursos identificados por **URIs**
- 🔹 Representações de dados, como **JSON**

---

## 📡 Protocolo HTTP

**HTTP (Hypertext Transfer Protocol)** é o protocolo que permite a comunicação na World Wide Web.

Ele estabelece as regras para que clientes, como navegadores, e servidores troquem informações.

### Conceitos principais

- 🧑‍💻 **Cliente-servidor:** o navegador faz requisições aos servidores Web.
- 🔄 **Stateless:** cada requisição é independente.
- 📝 **Baseado em texto:** as mensagens são legíveis por humanos.

---

## 🛣️ Métodos HTTP

| Método | Finalidade | Característica |
|---|---|---|
| `GET` | Recuperar informações | Seguro e idempotente |
| `POST` | Criar novos recursos | Não idempotente |
| `PUT` | Substituir completamente um recurso | Atualização |
| `PATCH` | Atualizar parcialmente um recurso | Atualização |
| `DELETE` | Remover um recurso | Idempotente |

### 💡 Exemplo rápido

```text
GET     → consultar
POST    → criar
PUT     → substituir
PATCH   → atualizar parcialmente
DELETE  → remover
```

---

## 🎯 Endpoint

Um **endpoint** é uma URL específica que fornece acesso a um recurso ou funcionalidade de uma API.

Ele representa o ponto de comunicação entre o cliente e o servidor.

### 🔗 Exemplo citado na aula

https://github.com/awesomeapibrasil/awesomeapi-cep

---

## 🗂️ APIs Públicas

Catálogos de APIs públicas ajudam no estudo e no desenvolvimento de aplicações reais.

Eles reúnem APIs disponibilizadas por diferentes projetos e serviços para que desenvolvedores encontrem fontes de dados para integrar às suas aplicações.

### 🔗 Catálogo

https://www.freepublicapis.com/

---

## 📦 JSON

**JSON (JavaScript Object Notation)** é um formato leve para troca de dados.

Características:

- 👀 Fácil para humanos lerem e escreverem
- 🤖 Fácil para máquinas interpretarem e gerarem
- 🧱 Trabalha com objetos, usando pares **nome/valor**
- 📋 Trabalha com **arrays**, que são listas ordenadas de valores

### Exemplo

```json
{
  "nome": "João",
  "idade": 20,
  "tecnologias": ["HTML", "CSS", "JavaScript"]
}
```

---

## 🔄 Como funciona uma requisição

O fluxo apresentado na aula pode ser entendido assim:

```text
👤 Usuário
   ↓
🖥️ Front-end / Navegador
   ↓
📡 Requisição HTTP
   ↓
⚙️ Servidor Express.js
   ↓
🗄️ Banco de Dados / API Externa
   ↓
📦 Resposta JSON
   ↓
🖥️ Front-end atualiza a tela
```

### Etapas

1. 🌐 O usuário acessa a página ou interage com o sistema.
2. 📡 O navegador envia uma requisição HTTP.
3. ⚙️ O servidor recebe a requisição, identifica a rota e executa a lógica.
4. 🗄️ O servidor busca, grava ou atualiza informações.
5. 📦 O servidor retorna os dados, normalmente em JSON.
6. 🖥️ O front-end recebe a resposta e apresenta os dados ao usuário.

---

## 🖥️ Backend e Web Service

### ⚙️ Servidor Backend

É o sistema responsável por:

- Armazenar e recuperar dados
- Executar regras de negócio
- Fornecer APIs para comunicação
- Processar requisições
- Fornecer respostas para clientes

### 🌐 Web Service

É um serviço acessível pela Web que permite a comunicação entre sistemas utilizando HTTP/HTTPS.

Isso possibilita que sistemas heterogêneos, desenvolvidos com diferentes linguagens, plataformas ou tecnologias, se comuniquem de maneira padronizada.

---

## 🚀 Express.js

**Express.js** é um framework para **Node.js** que facilita a criação de servidores Web e APIs.

Características destacadas:

- 🧩 Minimalista
- 🔧 Flexível
- 🌎 Popular no ecossistema JavaScript
- 🛣️ Facilita o roteamento
- 🔌 Utiliza middlewares
- ⚡ Ajuda na criação rápida de APIs e servidores

### 📦 Instalação

```bash
npm install express
```

### 🌐 CORS

Para trabalhar com acesso entre domínios diferentes no navegador:

```bash
npm install cors express
```

> **CORS** é um mecanismo de segurança que controla o acesso entre diferentes domínios no navegador.

### ▶️ Executando a API

```bash
node api.js
```

---

## ☁️ Render

O **Render** é apresentado na aula como uma plataforma de hospedagem em nuvem que pode ser utilizada para simular e disponibilizar Web Services.

Características apresentadas:

- ☁️ Hospedagem em nuvem
- 🔗 Integração com repositórios Git
- 🚀 Deploy contínuo
- 🔒 Certificado SSL
- 📈 Possibilidade de escalabilidade
- 🎓 Adequado para projetos acadêmicos

### 🔗 Acesso

https://render.com/

### 🔗 Dashboard

https://dashboard.render.com/

### 🚀 Fluxo de deploy

1. 📦 Faça o commit do projeto no GitHub.
2. ☁️ Crie uma conta no Render.
3. 🔗 Conecte o repositório do GitHub.
4. 🛠️ Crie um **Web Service**.
5. ▶️ Configure os comandos de execução.
6. 🚀 Faça o deploy.
7. 🌐 Utilize a URL gerada pelo Render, como:
   `seu-projeto.onrender.com`

### ⚙️ Comandos indicados na aula

```text
Build Command: node
Start Command: node api.js
```

---

# 📝 Atividade 01

## 🎯 Objetivo

Pesquisar **10 projetos no GitHub** que utilizem algum tipo de API em suas aplicações.

### 📋 O que fazer

- 🔎 Pesquisar 10 projetos no GitHub.
- 📥 Clonar os projetos.
- 🔍 Analisar os projetos.
- 🧩 Identificar o framework utilizado.
- 🔌 Identificar as APIs consumidas.
- 📝 Criar um arquivo Markdown.
- 📊 Criar uma tabela detalhando os projetos escolhidos e suas informações.

## 📊 Modelo de tabela

| # | Projeto | GitHub | Framework | API consumida | Observações |
|---:|---|---|---|---|---|
| 1 | Projeto 01 | 🔗 [Acessar](#) | — | — | — |
| 2 | Projeto 02 | 🔗 [Acessar](#) | — | — | — |
| 3 | Projeto 03 | 🔗 [Acessar](#) | — | — | — |
| 4 | Projeto 04 | 🔗 [Acessar](#) | — | — | — |
| 5 | Projeto 05 | 🔗 [Acessar](#) | — | — | — |
| 6 | Projeto 06 | 🔗 [Acessar](#) | — | — | — |
| 7 | Projeto 07 | 🔗 [Acessar](#) | — | — | — |
| 8 | Projeto 08 | 🔗 [Acessar](#) | — | — | — |
| 9 | Projeto 09 | 🔗 [Acessar](#) | — | — | — |
| 10 | Projeto 10 | 🔗 [Acessar](#) | — | — | — |

> 🔒 Os links `#` estão **reservados** para você inserir os links reais dos projetos.

---

# 📝 Atividade 02

## 🎯 Objetivo

Criar uma API usando **Express**, fazer o deploy no **Render** e desenvolver um front-end que consuma essa API.

### 📋 Requisitos

1. 🚀 Criar uma API utilizando Express.
2. 🕐 Criar uma rota para consulta de **data e hora**.
3. ☁️ Fazer o deploy da API no Render.
4. 🔗 Conectar o Render ao repositório do GitHub.
5. 🖥️ Desenvolver uma aplicação front-end.
6. 🔌 Fazer o front-end consumir a API.
7. 📅 Apresentar na tela a data e a hora.
8. 📦 Utilizar outro repositório para separar a API do front-end.
9. 📸 Organizar prints do código e da aplicação funcionando.
10. ☁️ Adicionar prints dos painéis do Render e Vercel.
11. 🔗 Informar os links dos repositórios no GitHub.
12. 📤 Enviar a atividade na plataforma CANVA.

---

# 🔗 Links dos projetos

> Esta seção fica **reservada para os links finais dos seus projetos**.

### 🧩 Projeto 01 — API

🔗 **GitHub:** [(https://github.com/ronaldorfas/API-express)]

🔗 **Render:** `COLE_AQUI_O_LINK_DO_RENDER`

### 🖥️ Projeto 01 — Front-end

🔗 **GitHub:** [(https://github.com/ronaldorfas/Projetocom-API)]

🔗 **Vercel:** `COLE_AQUI_O_LINK_DA_VERCEL`

---

## 📌 Resumo para revisão

```text
API
└── Permite comunicação entre diferentes componentes de software.

REST
└── Estilo arquitetural usado em sistemas distribuídos.

HTTP
├── GET     → consultar
├── POST    → criar
├── PUT     → substituir
├── PATCH   → atualizar parcialmente
└── DELETE  → remover

ENDPOINT
└── URL específica de acesso a um recurso ou funcionalidade.

JSON
└── Formato leve para troca de dados.

BACKEND
└── Processa requisições, regras de negócio e dados.

EXPRESS.JS
└── Framework Node.js para criação de servidores e APIs.

CORS
└── Controla acesso entre diferentes domínios no navegador.

RENDER
└── Plataforma utilizada para hospedagem/deploy de Web Services.

ATIVIDADE 01
└── Pesquisar e analisar 10 projetos GitHub que utilizam APIs.

ATIVIDADE 02
└── Criar API + deploy no Render + Front-end consumindo a API.
```

---

## 🔗 Links principais

- 🌐 [Free Public APIs](https://www.freepublicapis.com/)
- 💻 [Exemplo de API de CEP no GitHub](https://github.com/awesomeapibrasil/awesomeapi-cep)
- ☁️ [Render](https://render.com/)
- 🖥️ [Render Dashboard](https://dashboard.render.com/)
- 🐙 [GitHub](https://github.com/)
- ▲ [Vercel](https://vercel.com/)

---

## 📚 Referência da aula

**Consumindo APIs no Front-end — Frameworks Front-end**  
Prof. Me. Deivison S. Takatu

📧 deivison.takatu@edu.senai.br
