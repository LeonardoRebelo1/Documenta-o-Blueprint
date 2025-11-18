# 🤖 RepoAnalyst (Blueprint)

![Status: Em Design](https://img.shields.io/badge/status-Em%20Design-blue.svg)
![Tecnologia Planejada: Python](https://img.shields.io/badge/tech-Python-3776AB.svg?logo=python)
![Tecnologia Planejada: React](https://img.shields.io/badge/tech-React-61DAFB.svg?logo=react)

O **RepoAnalyst** é um sistema de software como serviço (SaaS) planejado para usar Inteligência Artificial para analisar repositórios de código-fonte do GitHub, fornecendo insights sobre a qualidade do código, saúde do projeto e padrões de contribuição.

**Este repositório contém a Documentação Blueprint do sistema. O código-fonte ainda não foi iniciado.**

## 🗺️ Visão Geral do Sistema

O objetivo é conectar-se ao GitHub (via OAuth), clonar um repositório, analisá-lo com um pipeline de IA e apresentar um dashboard com métricas acionáveis para o proprietário do repositório.

## 📚 Documentação de Domínio

Para entender o design e o escopo do `RepoAnalyst`, consulte os documentos de blueprint em nossa pasta `/docs`:

* **[📄 Arquitetura do Sistema](./docs/ARCHITECTURE.md)**:
    Visão de alto nível dos componentes do sistema e como eles interagem.
* **[🔌 Definição da API](./docs/API.md)**:
    O contrato de como o front-end se comunicará com o back-end.
* **[🧊 Modelos de Dados](./docs/DATA_MODELS.md)**:
    As entidades centrais do nosso sistema (Usuário, Repositório, Análise).
* **[🧑‍💻 Histórias de Usuário](./docs/USER_STORIES.md)**:
    O que o sistema *deve fazer* da perspectiva do usuário final.

## 🚀 Roteiro (Roadmap) Proposto

1.  **Q1 (Design):** Finalizar este Blueprint.
2.  **Q2 (Desenvolvimento):** Implementar o Módulo de Autenticação e o Módulo de Análise (Core).
3.  **Q3 (Desenvolvimento):** Construir o Dashboard de Visualização (React).
4.  **Q4 (Lançamento):** Beta fechado.


flowchart TD
    A[Christmas] -->|Get money| B(Go shopping)
    B --> C{Let me think}
    C -->|One| D[Laptop]
    C -->|Two| E[iPhone]
    C -->|Three| F[fa:fa-car Car]
  
