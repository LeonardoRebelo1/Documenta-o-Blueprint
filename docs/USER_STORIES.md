# 🧑‍💻 Domínio: Histórias de Usuário

Este documento descreve as funcionalidades do `RepoAnalyst` da perspectiva do usuário final. Ele define o "o quê" (e por que) o sistema deve fazer.

## Persona Principal
* **Persona:** `Desenvolvedor / Dono de Repositório` (chamado de "Usuário").
* **Objetivo:** Entender rapidamente a saúde do seu projeto e onde focar os esforços de melhoria.

---

### Módulo: Autenticação e Onboarding

* **US-101 (Login):**
    > **Como um** novo usuário,
    > **Eu quero** me cadastrar/logar usando minha conta do GitHub,
    > **Para que** eu não precise criar e lembrar de outra senha.

* **US-102 (Listar Repos):**
    > **Como um** usuário logado,
    > **Eu quero** ver uma lista dos meus repositórios públicos e privados (que eu autorizei),
    > **Para que** eu possa escolher qual deles analisar.

### Módulo: Análise de Repositório

* **US-201 (Solicitar Análise):**
    > **Como um** usuário,
    > **Eu quero** clicar em um botão "Analisar Agora" ao lado de um dos meus repositórios,
    > **Para que** o sistema inicie uma nova verificação de qualidade.

* **US-202 (Ver Status da Análise):**
    > **Como um** usuário que acabou de solicitar uma análise,
    > **Eu quero** ver um indicador de status (ex: "Processando", "Na fila"),
    > **Para que** eu saiba que o sistema está trabalhando e não travei o aplicativo.
    * **Critério de Aceitação:** O status deve ser atualizado automaticamente (via polling ou websocket) ou com um F5.

### Módulo: Dashboard (Resultados)

* **US-301 (Ver Relatório):**
    > **Como um** usuário,
    > **Eu quero** ser direcionado para uma página de "Relatório" quando a análise estiver concluída,
    > **Para que** eu possa ver os resultados.

* **US-302 (Pontuação Geral):**
    > **Como um** usuário que está vendo um relatório,
    "Eu quero" ver uma pontuação de qualidade geral (ex: 85/100) em destaque,
    **Para que** eu possa ter uma avaliação rápida da saúde do projeto.

* **US-303 (Ver "Hotspots"):**
    > **Como um** usuário que está vendo um relatório,
    > **Eu quero** ver uma lista de "pontos críticos" ou "problemas" (ex: arquivos mais complexos, funções com problemas),
    > **Para que** eu saiba exatamente onde o código precisa de atenção.
    * **Critério de Aceitação:** Cada item da lista deve mostrar o nome do arquivo, a linha e o tipo de problema.

* **US-304 (Histórico de Análise):**
    > **Como um** usuário,
    > **Eu quero** ver um gráfico simples mostrando a pontuação de qualidade ao longo do tempo (últimas 5 análises),
    > **Para que** eu possa ver se o projeto está melhorando ou piorando.