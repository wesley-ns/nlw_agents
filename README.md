# NLW Agents

> Projeto desenvolvido durante o evento NLW da RocketSeat.

## Tecnologias e Bibliotecas Utilizadas

- **Node.js** (runtime)
- **TypeScript** (tipagem estática)
- **Fastify** (framework web)
- **Drizzle ORM** (ORM para banco de dados)
- **PostgreSQL** (banco de dados relacional)
- **Zod** (validação de dados)
- **@fastify/cors** (CORS middleware)
- **drizzle-kit** (migrations e geração de schema)
- **docker** (ambiente de banco de dados)

## Padrões de Projeto

- Organização por responsabilidade (ex: `db/`, `http/`, `schema/`)
- Validação de dados com Zod
- Migrations e seeds com Drizzle ORM

## Setup e Configuração

1. **Clone o repositório:**
   ```bash
   git clone <url-do-repositorio>
   cd nlw_agents_server
   ```
2. **Instale as dependências:**
   ```bash
   npm install
   ```
3. **Configure o ambiente:**
   - Copie `.env.example` para `.env` e ajuste as variáveis se necessário.
4. **Suba o banco de dados com Docker:**
   ```bash
   docker-compose up -d
   ```
5. **Rode as migrations e seeds:**
   ```bash
   npm drizzle-kit migrate
   npm run db:seed
   ```
6. **Inicie o servidor em modo desenvolvimento:**
   ```bash
   npm run dev
   ```

## Scripts Disponíveis

- `npm run dev` — Inicia o servidor em modo desenvolvimento
- `npm start` — Inicia o servidor em modo produção
- `npm run db:seed` — Executa o seed do banco de dados

## Endpoints

O servidor estará disponível em `http://localhost:3333`.

- `GET /health` - Health check da aplicação
- `GET /rooms` - Lista as salas disponíveis

Desenvolvido durante o NLW da RocketSeat.