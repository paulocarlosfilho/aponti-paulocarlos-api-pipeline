# Delivery API 🚚

[![CI/CD](https://github.com/actions/workflows/pipeline.yml/badge.svg)](https://github.com/actions/workflows/pipeline.yml)
[![Node.js](https://img.shields.io/badge/Node.js-20.x-blue.svg)](https://nodejs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.x-blue.svg)](https://www.typescriptlang.org/)
[![Express.js](https://img.shields.io/badge/Express.js-4.x-green.svg)](https://expressjs.com/)
[![Jest](https://img.shields.io/badge/Jest-30.x-red.svg)](https://jestjs.io/)
[![ESLint](https://img.shields.io/badge/ESLint-10.x-purple.svg)](https://eslint.org/)

## 📝 Descrição

**Delivery API** é uma API RESTful para gerenciamento de pedidos de um serviço de delivery. Construída com Node.js, Express e TypeScript, esta API oferece uma base sólida e escalável para aplicações de delivery.

## ✨ Funcionalidades

- **Listar todos os pedidos:** Obtenha uma lista de todos os pedidos cadastrados.
- **Obter um pedido por ID:** Busque um pedido específico pelo seu identificador único.
- **Criar um novo pedido:** Adicione um novo pedido ao sistema.

## 🚀 Começando

Siga estas instruções para obter uma cópia do projeto em funcionamento na sua máquina local para desenvolvimento e testes.

### 📋 Pré-requisitos

Antes de começar, certifique-se de ter as seguintes ferramentas instaladas:

- [Node.js](https://nodejs.org/) (versão 20.x ou superior)
- [npm](https://www.npmjs.com/) (geralmente vem com o Node.js)

### ⚙️ Instalação

1. **Clone o repositório:**
   ```bash
   git clone <url-do-repositorio>
   ```
2. **Navegue até o diretório do projeto:**
   ```bash
   cd delivery-api
   ```
3. **Instale as dependências:**
   ```bash
   npm install
   ```

## ▶️ Uso

### Scripts Disponíveis

No diretório do projeto, você pode rodar os seguintes scripts:

| Script | Descrição |
| :--- | :--- |
| `npm run dev` | Inicia a aplicação em modo de desenvolvimento com hot-reloading. |
| `npm start` | Inicia a aplicação em modo de produção (requer build prévio). |
| `npm run build` | Compila o código TypeScript para JavaScript na pasta `dist`. |
| `npm test` | Executa os testes unitários e de integração com o Jest. |
| `npm run lint` | Analisa o código com o ESLint para garantir a qualidade e o padrão. |

### Iniciando o Servidor

Para iniciar o servidor em modo de desenvolvimento, execute:

```bash
npm run dev
```

A API estará disponível em `http://localhost:3000`.

## Endpoints da API

A seguir estão os endpoints disponíveis na API:

| Método | Endpoint | Descrição |
| :--- | :--- | :--- |
| `GET` | `/api/orders` | Retorna uma lista de todos os pedidos. |
| `GET` | `/api/orders/:id` | Retorna um pedido específico com base no ID. |
| `POST` | `/api/orders` | Cria um novo pedido. |

**Exemplo de corpo da requisição para `POST /api/orders`:**

```json
{
  "customerName": "João da Silva",
  "items": [
    { "name": "Pizza de Calabresa", "quantity": 1 },
    { "name": "Refrigerante", "quantity": 2 }
  ],
  "total": 55.00
}
```

## 🧪 Testes

Para rodar a suíte de testes, execute o seguinte comando:

```bash
npm test
```

## 🏗️ Estrutura do Projeto

```bash
.
├── .github/
│   └── workflows/
│       └── pipeline.yml  # Workflow de CI/CD
├── dist/                 # Arquivos compilados para produção
├── node_modules/         # Dependências do projeto
├── src/                  # Código-fonte da aplicação
│   └── server.ts         # Arquivo principal do servidor
├── .gitignore
├── eslint.config.mjs     # Configuração do ESLint
├── jest.config.js        # Configuração do Jest
├── package-lock.json
├── package.json          # Metadados e dependências do projeto
└── tsconfig.json         # Configuração do TypeScript
```

## 🔄 CI/CD

Este projeto utiliza **GitHub Actions** para integração e entrega contínua. O workflow, definido em `.github/workflows/pipeline.yml`, é acionado a cada `push` ou `pull request` na branch `main` e executa as seguintes etapas:

1. **Checkout do código**
2. **Setup do ambiente Node.js**
3. **Instalação de dependências**
4. **Execução do Linter**
5. **Execução dos testes**
6. **Build do projeto**

Isso garante que todo código novo seja testado e esteja em conformidade com os padrões de qualidade antes de ser integrado.

## 🤝 Contribuição

Contribuições são o que tornam a comunidade de código aberto um lugar incrível para aprender, inspirar e criar. Qualquer contribuição que você fizer será **muito apreciada**.

1. Faça um **Fork** do projeto
2. Crie uma **Branch** para sua feature (`git checkout -b feature/AmazingFeature`)
3. Faça o **Commit** de suas alterações (`git commit -m 'Add some AmazingFeature'`)
4. Faça o **Push** para a Branch (`git push origin feature/AmazingFeature`)
5. Abra um **Pull Request**

---

Feito com ❤️ por [Seu Nome](https://github.com/paulocarlosfilho)