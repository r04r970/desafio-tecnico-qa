# BIX Mini E-commerce - Desafio Técnico QA

Um mini e-commerce com funcionalidades de autenticação, gestão de estoque, sistema de cupons de desconto e testes automatizados de QA.

## 🚀 Funcionalidades Implementadas

### ✅ Autenticação de Usuários

* Sistema de login/logout
* Sessões persistentes com localStorage
* Proteção de rotas para checkout
* Testes automatizados de login e logout

### ✅ Gestão de Estoque

* Controle de quantidade disponível por produto
* Validação de estoque em tempo real
* Atualização automática após compras
* Interface adaptativa (botões desabilitados quando sem estoque)
* Testes automatizados de quantidade e validação de estoque

### ✅ Sistema de Cupons de Desconto

* Cupons de desconto percentual e valor fixo
* Validação de cupons ativos/expirados
* Aplicação automática no checkout
* Cálculo de subtotal, desconto e total final
* Testes automatizados de aplicação e validade de cupons

### ✅ Carrinho de Compras

* Adição múltipla de produtos
* Validação de quantidade vs estoque
* Cálculo automático de totais
* Limpeza automática após checkout
* Testes automatizados de fluxo do carrinho e checkout

## 🛠️ Tecnologias

* **Backend**: Node.js + Express
* **Frontend**: HTML5 + CSS3 + JavaScript Vanilla
* **Automação de Testes**: Playwright + TypeScript
* **Containerização**: Docker + Docker Compose

## 📋 Pré-requisitos

* Docker e Docker Compose instalados
* Node.js e npm instalados

## 🚀 Como Executar

### Docker

```bash
# Clone o repositório
git clone https://github.com/r04r970/desafio-tecnico-qa-bixtecnologia.git
cd desafio-tecnico-qa-bixtecnologia/playwright

# Execute com Docker
docker compose up --build

# Acesse a aplicação
open http://localhost:3001
```

### Local (sem Docker)

```bash
# Instalar dependências
docker compose up --build
npm install

# Executar aplicação
npm start
```

### Executar Testes Automatizados

```bash
# Testes E2E
npx playwright test tests/e2e --headed --debug

# Testes de API
npx playwright test tests/api --headed --debug
```

## 👤 Credenciais de Teste

### Usuários Disponíveis

* **Admin**: `admin@test.com` / `admin123`
* **Usuário**: `user@test.com` / `user123`

### Cupons de Desconto

* `WELCOME10` - 10% de desconto
* `SAVE20` - 20% de desconto
* `FIXED50` - R$ 50,00 de desconto fixo
* `EXPIRED` - Cupom expirado (para testes)

## 📡 API Endpoints

### Autenticação

* `POST /api/login` - Login de usuário
* `POST /api/logout` - Logout de usuário
* `GET /api/me` - Informações do usuário logado

### Produtos

* `GET /api/products` - Lista de produtos com estoque

### Cupons

* `POST /api/validate-coupon` - Validar cupom de desconto

### Checkout

* `POST /api/checkout` - Finalizar compra com validação de estoque e cupons

### Health Check

* `GET /api/health` - Status da aplicação

## 🏗️ Arquitetura

```
qa-test/
├── backend/
│   ├── data/           # Dados JSON (produtos, usuários, cupons)
│   ├── public/         # Frontend estático
│   └── server.js       # Servidor Express
├── tests/              # Testes automatizados E2E e API
├── docker-compose.yml  # Configuração Docker
└── Dockerfile          # Imagem Docker
```

## 📝 Próximos Passos

* Adicionar mais testes automatizados cobrindo cenários críticos adicionais
* Integrar CI/CD para execução automática dos testes

## 📄 Licença

Este projeto é parte do processo seletivo da BIX.
