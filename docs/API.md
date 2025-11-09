# 🔌 Domínio: Definição da API (Contrato)

Este documento define os *endpoints* da API que o `RepoAnalyst` irá expor. Esta é a "planta" para o desenvolvimento de back-end e front-end.

**Base URL (Proposta):** `https://api.repoanalyst.com/v1`

## Autenticação

* **Esquema:** Bearer Token (JWT)
* `POST /auth/github/callback`: Rota para o callback do GitHub OAuth. Retorna um JWT.

## Repositórios

* `GET /repos`: Lista os repositórios do usuário autenticado (puxados do GitHub).
    * **Resposta (200):**
        ```json
        {
          "data": [
            { "id": "gh_123", "full_name": "usuario/meu-repo", "last_analyzed": null }
          ]
        }
        ```

* `POST /repos/analyze`: Solicita uma nova análise para um repositório.
    * **Corpo da Requisição:**
        ```json
        { "repo_full_name": "usuario/meu-repo" }
        ```
    * **Resposta (202 - Accepted):** A análise foi enfileirada, não concluída.
        ```json
        { "status": "pending", "job_id": "uuid-1234-abcd" }
        ```

## Análises (Resultados)

* `GET /analysis/{job_id}/status`: Verifica o status de uma análise em andamento.
    * **Resposta (200):**
        ```json
        { "status": "processing", "progress": 45 }
        ```

* `GET /analysis/{repo_full_name}`: Pega o último relatório de análise completo para um repositório.
    * **Resposta (200):**
        ```json
        {
          "report_id": "report-xyz",
          "generated_at": "2025-11-06T20:00:00Z",
          "quality_score": 85,
          "hotspots": [
            { "file": "src/main.py", "line": 42, "issue": "Complexidade Ciclomática Alta" }
          ]
        }
        ```