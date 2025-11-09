# 🤝 Como Contribuir com o `RepoAnalyst`

Primeiramente, obrigado pelo seu interesse em contribuir! Embora este projeto esteja atualmente em fase de **Blueprint (Design)**, as contribuições para o design e planejamento são muito bem-vindas.

Quando o desenvolvimento começar, este documento definirá o processo.

## Código de Conduta

Esperamos que todos os participantes sigam nosso **[Código de Conduta](./CODE_OF_CONDUCT.md)** (A ser criado). Por favor, seja respeitoso e profissional.

## 💬 Sugerindo Mudanças no Blueprint

Nesta fase, a melhor forma de contribuir é melhorando esta documentação.

* **Encontrou uma falha no design?**
* **Vê um problema na arquitetura proposta?**
* **Acha que um endpoint da API está faltando?**

Abra uma **Issue** no GitHub descrevendo sua sugestão. Use a label `design-proposal`.

## 🚀 Como Contribuir com Código (Processo Futuro)

Quando o desenvolvimento de código começar, seguiremos este fluxo:

### 1. Stack Tecnológica Planejada

* **Frontend:** React (com TypeScript)
* **Backend (Serviços):** Python 3.11+ (usando FastAPI)
* **Banco de Dados:** PostgreSQL
* **Fila:** RabbitMQ
* **Infraestrutura:** Docker e (provavelmente) Kubernetes

### 2. Fluxo de Trabalho (Git Workflow)

1.  **Nunca commit direto na `main`:** A branch `main` será protegida.
2.  **Crie uma Branch:** Faça um fork do repositório e crie uma branch a partir da `main`.
    * Use prefixos: `feat/` (novas features), `fix/` (correção de bugs), `docs/` (mudanças na documentação).
    * *Exemplo:* `git checkout -b feat/user-login-jwt`
3.  **Desenvolva e Commite:** Escreva seu código. Siga o padrão de [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/).
    * *Exemplo:* `feat: adiciona endpoint de autenticação /auth/callback`
4.  **Abra um Pull Request (PR):** Envie seu PR para a branch `main` do repositório principal.
5.  **Revisão de Código:** Pelo menos um outro membro da equipe (mantenedor) precisará revisar e aprovar seu PR.
6.  **Merge:** Após a aprovação, seu código será integrado à `main`.