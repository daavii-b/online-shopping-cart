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

## Como rodar o projeto

1. Siga as instruções de cada subprojeto:
   - [shopping-backend/README.md](./shopping-backend/README.md)
   - [shopping-frontend/README.md](./shopping-frontend/README.md)

## Observações

- Cada submódulo tem seu próprio histórico de commits preservado.
