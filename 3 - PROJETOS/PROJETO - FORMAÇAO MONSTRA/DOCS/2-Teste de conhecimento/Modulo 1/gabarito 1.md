# 📚 Gabarito Comentado: Módulo 1 – Melhores Práticas de Hiperautomação

Este documento consolida as análises das Provas 1, 2 e 3 do Módulo 1, focando em estratégia, arquitetura de solução, governança e decisão técnica.

---

## 📝 Prova 1: Fundamentos e Seleção de Ferramentas

### 1. Sistema Legado sem API

**Cenário:** Automatizar verificação de status em sistema "green-screen" legado.

* **Resposta Correta:** **B. MuleSoft RPA with screen automation**
* **Análise:** O RPA é o "braço" digital para sistemas onde não há APIs (Mainframes, Desktop). Composer e Flow exigem conectores ou APIs.

### 2. Sincronização No-Code SaaS

**Cenário:** Sincronizar objetos entre Salesforce e NetSuite rapidamente, sem código.

* **Resposta Correta:** **C. MuleSoft Composer with prebuilt SaaS connectors**
* **Análise:** O Composer é focado em *Business Users* e agilidade para integrar nuvens modernas (SaaS) usando conectores nativos.

### 3. Alto Volume de Dados

**Cenário:** Processar milhões de registros transacionais noturnos com agregação.

* **Resposta Correta:** **C. Anypoint Platform APIs with batch processing**
* **Análise:** Anypoint é o "cérebro". É a única robusta o suficiente para lidar com milhões de registros e lógica complexa de agregação (*Batch*).

### 4. Governança e C4E (Reuso de Login)

**Cenário:** Evitar múltiplos logins para o mesmo ERP em automações diferentes.

* **Resposta Correta:** **B. Reuse a shared RPA process published in Anypoint Exchange**
* **Análise:** O modelo C4E prega o reuso. Publicar ativos no Exchange permite que outras equipes consumam a lógica sem duplicar esforço.

### 5. Dimensões da Matriz: Composer

**Cenário:** Justificar o uso do Composer para mapeamento simples entre Salesforce e ServiceNow.

* **Resposta Correta:** **B. Complexidade e Perfil do Usuário**
* **Análise:** Composer é ideal para baixa complexidade e usuários de negócio (*Admins*).

### 6. Resiliência: Banco de Dados Instável

**Cenário:** Minimizar o impacto de um banco de dados local "flaky" (instável).

* **Resposta Correta:** **B. Implement exponential backoff and retries in the API**
* **Análise:** Erros técnicos de conexão são resolvidos com lógica de retentativa crescente para não sobrecarregar o sistema.

### 7. Testes: Sistema não disponível

**Cenário:** Garantir testes E2E antes do sistema legado estar pronto.

* **Resposta Correta:** **B. Anypoint Exchange Mocking Service**
* **Análise:** O *Mocking Service* simula a resposta da API, permitindo que o desenvolvimento do front-end continue em paralelo.

### 8. Classificação de Erros

**Cenário:** O robô falhou ao tentar abrir uma janela desktop.

* **Resposta Correta:** **C. Technical exception in the RPA layer**
* **Análise:** Falhas de interface ou infraestrutura do robô são classificadas como exceções técnicas na camada RPA.

### 9. API-Led: Reuso de Dados

**Cenário:** Chatbot precisa de dados já disponíveis em uma System API estável.

* **Resposta Correta:** **C. Create an Experience API on top of the existing System API**
* **Análise:** Nunca duplique a integração. Crie uma camada de experiência que consuma a System API já existente.

### 10. Idempotência

**Cenário:** Evitar processamento duplicado caso a mesma mensagem seja enviada duas vezes.

* **Resposta Correta:** **A. Idempotency of API operations**
* **Análise:** Idempotência garante que chamadas repetidas com o mesmo ID não gerem efeitos colaterais duplicados.

### 11. Isolamento de Erro em Testes E2E

**Cenário:** Maneira mais eficiente de identificar falhas em um fluxo longo.

* **Resposta Correta:** **C. Validate RPA, integration APIs and target systems independently**
* **Análise:** Testar as camadas isoladamente permite identificar rapidamente o ponto exato da falha.

### 12. Orquestração de Longa Duração

**Cenário:** Processo com aprovação humana (dias) + chamada técnica.

* **Resposta Correta:** **A. Salesforce Flow Orchestration**
* **Análise:** O Orchestrator gerencia processos complexos de múltiplos estágios e longa duração (dias/semanas).

### 13. Responsabilidade das Camadas (API-Led)

**Cenário:** Onde colocar transformações pesadas e agregação?

* **Resposta Correta:** **B. Process APIs are responsible for orchestration and business logic**
* **Análise:** System APIs devem ser "enxutas" (apenas desbloqueiam dados); a Process API detém a lógica de negócio.

---

---

## 📝 Prova 2: Estratégia e Arquitetura

| Questão | Resposta Correta | Justificativa Curta |
| --- | --- | --- |
| **Ponto-a-ponto para Governança** | **C** (API-led Connectivity) | Organiza integrações frágeis em camadas governadas. |
| **Exposição de Preços Multicanal** | **C** (System API + Experience APIs) | Maximiza o reuso do acesso ao dado para diferentes canais. |
| **Lógica Complexa no Composer?** | **C** (Process API no Anypoint) | Composer não é feito para agregações pesadas; use o Anypoint. |
| **RPA para sistema com API REST** | **B** (Preferir API-first) | RPA é mais lento e frágil; use APIs se elas existirem. |
| **Estoque Near Real-Time** | **B** (System API + Composer) | Equilibra a robustez da API com a agilidade do Composer. |
| **Aprovação Humana (Vários dias)** | **B** (Flow Orchestration) | Ferramenta correta para estados de espera e interação humana. |
| **Responsável pelo Reuso** | **B** (C4E - Center for Enablement) | Equipe que define padrões e promove o catálogo de ativos. |
| **Resiliência em Carga Alta** | **B** (Retries + Backoff) | Protege o sistema e garante que a transação seja concluída. |
| **Dados de Teste Seguros** | **B** (Synthetic/Mock Data) | Evita riscos de privacidade e segurança (LGPD). |
| **SaaS-to-SaaS (Admin Owner)** | **B** (MuleSoft Composer) | Melhor custo-benefício para integrações simples e rápidas. |
| **Tratamento de Erro Centralizado?** | **B** (Cada camada trata o seu) | Facilita o debug e mantém a independência dos módulos. |
| **Evitar Logins Duplicados** | **A** (Anypoint Exchange) | Catálogo central para compartilhar ativos e processos. |

---

## 📝 Prova 3: Decisão Técnica e Pegadinhas de Exame

### ⚡ Análise de "Armadilhas" (Traps)

* **Reconstruir do Zero:** Se uma questão sugere criar algo que já existe, está errada. **Foque no Reuso.**
* **Complexidade Desnecessária:** Se um *Screen Flow* resolve com uma chamada simples, não adicione *Orchestrator*.
* **Bypass de Camadas:** Pular a camada de *Process* para ganhar performance é um erro de arquitetura a longo prazo.

### 💡 Conceitos Vitais

1. **Engagement Layer:** O Salesforce (Screen Flows) deve ser a interface principal para o usuário, não o RPA.
2. **Experience API:** Deve ser "leve", apenas formatando dados para o consumidor final.
3. **One-time Migration:** Para migrações únicas (CSV), use ferramentas nativas (Data Loader), não arquitetura de APIs.
4. **Governança Pós-Go-Live:** O C4E deve revisar o Exchange continuamente para garantir que os padrões são seguidos.

---