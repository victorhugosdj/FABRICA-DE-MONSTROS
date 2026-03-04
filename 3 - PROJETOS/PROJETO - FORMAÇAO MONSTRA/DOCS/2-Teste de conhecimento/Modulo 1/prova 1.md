---
# 📝 Prova 1 – Módulo 1: Melhores Práticas de Hiperautomação
---

1. AnyAirlines wants to automate checking customer loyalty status in a legacy green‑screen system with no APIs. What is the most appropriate primary technology?
   A. MuleSoft Composer calling a REST API  
   B. MuleSoft RPA with screen automation  
   C. Salesforce Flow with HTTP Callout  
   D. Anypoint Platform Experience API only  

2. Northern Trail Outfitters (NTO) wants to quickly sync standard objects between Salesforce and NetSuite using clicks, not code. Which solution best fits the requirement?
   A. Anypoint Studio with custom DataWeave transformations  
   B. MuleSoft RPA recording user actions in both systems  
   C. MuleSoft Composer with prebuilt SaaS connectors  
   D. Salesforce Flow with Scheduled Path and custom Apex  

3. A company needs to process millions of transaction records nightly, aggregating data from multiple databases. Which component should be the core of this integration?
   A. MuleSoft RPA with multiple bots in parallel  
   B. MuleSoft Composer flows triggered every 5 minutes  
   C. Anypoint Platform APIs with batch processing  
   D. Salesforce Flow invoked by Platform Events only  

4. A project team wants to avoid building multiple logins to the same legacy ERP for different automations. What is the best practice aligned with C4E?
   A. Embed login logic inside every bot individually  
   B. Reuse a shared RPA process published in Anypoint Exchange  
   C. Implement login logic in a Salesforce Screen Flow  
   D. Configure separate credentials in each Composer flow  

5. A customer asks: “We need the fastest no‑code way to connect Salesforce and ServiceNow with simple field mappings.” Which two dimensions from the tool selection matrix are most relevant to justify using Composer?
   A. Volume and Interface  
   B. Complexidade and Perfil do Usuário  
   C. Volume and Complexidade de Protocolo  
   D. Governança and Segurança Avançada  

6. NTO wants to minimize the impact of a flaky on‑premises database during request/response lookups in Anypoint APIs. What is the most efficient way to protect the consumer experience?
   A. Use RPA to read database screens instead of APIs  
   B. Implement exponential backoff and retries in the API  
   C. Move all logic into Salesforce Flows  
   D. Call the database directly from Composer on every request  

7. A solution architect wants to ensure end‑to‑end testing of a new hyperautomation scenario before the legacy system is ready. Which component should be used to simulate backend APIs?
   A. MuleSoft RPA Recorder  
   B. Anypoint Exchange Mocking Service  
   C. Salesforce Sandbox with only partial data  
   D. Production database with masked records  

8. In a complex flow involving Salesforce, RPA and Composer, one transaction failed. Logs show that the robot could not open a desktop window. How should the error be classified?
   A. Business exception  
   B. Integration exception  
   C. Technical exception in the RPA layer  
   D. Data quality exception  

9. A retail company already exposes a stable Customer System API on Anypoint. A new chatbot experience must reuse this data. What is the most efficient way to design the solution?
   A. Build a new System API specifically for the chatbot  
   B. Call the database directly from Einstein Bot  
   C. Create an Experience API on top of the existing System API  
   D. Use RPA to query the database with a headless client  

10. A bank wants to avoid duplicate processing if a request message is accidentally sent twice to an API that triggers RPA. Which concept is most important here?
    A. Idempotency of API operations  
    B. Horizontal scaling of workers  
    C. API proxying with Flex Gateway  
    D. Scheduler‑based throttling only  

11. In an end‑to‑end test of a hyperautomation flow, which is the most efficient way to isolate where an error occurred?
    A. Disable logs and enable only monitoring dashboards  
    B. Test the entire chain only from the user interface  
    C. Validate RPA, integration APIs and target systems independently  
    D. Retry the entire flow repeatedly until it passes  

12. A process involves a long‑running human approval plus a short, technical API call. When designing the architecture, which tool should handle the long‑running orchestration?
    A. Salesforce Flow Orchestration  
    B. MuleSoft Composer only  
    C. Anypoint Experience API  
    D. MuleSoft RPA Manager  

13. A candidate proposes putting all heavy data transformations into System APIs to keep Process APIs “thin”. Why is this not aligned with MuleSoft best practices?
    A. System APIs must not connect to any databases  
    B. Process APIs are responsible for orchestration and business logic  
    C. Experience APIs cannot perform transformations  
    D. RPA bots should handle transformations instead  

14. Which option best describes API‑led Connectivity in the context of hyperautomation?
    A. Direct point‑to‑point integrations between all systems  
    B. A layered model with System, Process and Experience APIs promoting reuse  
    C. A set of UI flows built only in Salesforce  
    D. A network of ungoverned webhooks between services  

15. During an exam question, a scenario offers four valid‑sounding options. Which one is most likely correct according to MuleSoft strategy?
    A. The option that recreates existing integrations from scratch  
    B. The option that maximizes reuse of existing APIs and assets  
    C. The option that adds the greatest number of new components  
    D. The option that ignores API‑led layers for speed
