<img src="https://i.postimg.cc/xT5jvJXF/rocketseat-logo-gray-dark.png" alt="Logo RocketSeat" width="160" align="left" style="padding-top:13px">

<img src="https://img.notionusercontent.com/s3/prod-files-secure%2Ff2d7c17c-c032-413b-bff4-03e44d1da06d%2F85695a90-803a-416c-8aef-3c9416ebbd3a%2FNLW_Agents.svg/size/?exp=1752183903&sig=cX-vEH7sm6ZiIVlQj8W8MQ4IoNFms6L7SBlBm4Cm36s&id=22a6c298-a282-807f-90cc-f974f0f40956&table=block&userId=4547f6a6-e638-4fb7-a23a-826dc5cf4188" alt="Logo NLW Agents" width="100" align="right">

<br><br>

## NLW Agents

Projeto desenvolvido durante um evento da **Rocketseat** utilizando tecnologias modernas para criação de uma API robusta e eficiente.

### 🚀 Tecnologias

- **Node.js** com TypeScript nativo (experimental strip types)
- **Fastify** - Framework web rápido e eficiente
- **PostgreSQL** com extensão **pgvector** para vetores
- **Drizzle ORM** - Type-safe database operations
- **Zod** - Schema validation
- **Docker** - Containerização do banco de dados
- **Biome** - Linting e formatação de código

### 🏗️ Arquitetura

O projeto segue uma arquitetura modular com:

- **Separação de responsabilidades** entre rotas, schemas e conexão com banco
- **Validação de schemas** com Zod para type safety
- **ORM type-safe** com Drizzle para operações de banco de dados
- **Validação de variáveis de ambiente** centralizadas

### ⚙️ Setup e Configuração

#### Pré-requisitos

- Node.js (versão com suporte a `--experimental-strip-types`)
- Docker e Docker Compose

#### 1. Clone o repositório

```bash
git clone <url-do-repositorio>
cd server
```

#### 2. Configure o banco de dados

```bash
docker-compose up -d
```

#### 3. Configure as variáveis de ambiente

Crie um arquivo `.env` na raiz do projeto:

```env
PORT=3333
DATABASE_URL=postgresql://docker:docker@localhost:5432/agents
```

#### 4. Instale as dependências

```bash
npm install
```

#### 5. Execute as migrações do banco

```bash
npx drizzle-kit migrate
```

#### 6. (Opcional) Popule o banco com dados de exemplo

```bash
npm run db:seed
```

### 7. Execute o projeto

**Desenvolvimento:**

```bash
npm run dev
```

**Produção:**

```bash
npm start
```

### 📚 Scripts Disponíveis

- `npm run dev` - Executa o servidor em modo de desenvolvimento com hot reload
- `npm start` - Executa o servidor em modo de produção
- `npm run db:seed` - Popula o banco de dados com dados de exemplo

### 🌐 Endpoints

A API estará disponível em `http://localhost:3333`

- `GET /health` - Health check da aplicação
- `GET /rooms` - Lista as salas disponíveis

---

Desenvolvido com 💜 durante o NLW da Rocketseatv
