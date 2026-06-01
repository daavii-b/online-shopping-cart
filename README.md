# 🛒 Online Shopping Cart Monorepo

Este repositório reúne os projetos **backend** e **frontend** como submódulos Git.

## Estrutura

```
online-shopping-cart/
├── shopping-backend/    # Submódulo: API NestJS
├── shopping-frontend/   # Submódulo: Frontend Next.js
├── .gitmodules
└── README.md
```

## Como clonar o monorepo

Clone o repositório principal **com os submódulos**:

```bash
git clone --recurse-submodules https://github.com/daavii-b/online-shopping-cart.git

cd online-shopping-cart
```

Se você já clonou sem `--recurse-submodules`, inicialize os submódulos assim:

```bash
git submodule update --init --recursive
```

## Como atualizar os submódulos

Para buscar as últimas alterações dos submódulos:

```bash
git submodule update --remote --merge
```

## Setup dos Projetos

### Backend (NestJS)

1. **Pré-requisitos:**
   - Node.js 20+
   - pnpm 9+
     - [Instalar Windows](https://pnpm.io/installation#on-windows)
     - [Instalar Linux](https://pnpm.io/installation#on-posix-systems)
     - [Instalar usando NPM](https://pnpm.io/installation#using-npm)
   - Docker e Docker Compose

2. **Instale as dependências:**

   ```bash
   cd shopping-backend
   pnpm install
   ```

3. **Variáveis de ambiente:**
   - Copie `.env.example` para `.env.development` e ajuste conforme necessário.

4. **Infraestrutura:**

   ```bash
   docker compose up -d
   ```

5. **Migrations e seeds:**

   ```bash
   pnpm migration:run
   pnpm seed
   ```

6. **Inicie a API:**

   ```bash
   pnpm start:dev
   ```

   - URL BASE: http://localhost:3001
   - API DOCS: http://localhost:3001/docs
   - Emails Inbox: http://localhost:8025

   **Endpoints**
   - `GET /api/v1/products` — Lista produtos
   - `GET /api/v1/cart` — Consulta carrinho
   - `PUT /api/v1/cart` — Atualiza carrinho
   - `POST /api/v1/orders` — Cria pedido

### Frontend (Next.js)

1. **Pré-requisitos:**
   - Node.js 20+
   - pnpm 9+

2. **Instale as dependências:**

   ```bash
   cd shopping-frontend
   pnpm install
   ```

3. **Variáveis de ambiente:**
   - Copie `.env.example` para `.env.local` e ajuste conforme necessário (ex: URL da API backend).

4. **Inicie o frontend:**

   ```bash
   pnpm dev
   # Ou produção: pnpm build && pnpm start
   ```

   - App: http://localhost:3000

## Como atualizar os submódulos

Para buscar as últimas alterações dos submódulos:

```bash
git submodule update --remote --merge
```

## Observações

- As pastas que começam com `shopping-` são submódulos Git (backend e frontend).
- Cada submódulo tem seu próprio histórico de commits preservado.
