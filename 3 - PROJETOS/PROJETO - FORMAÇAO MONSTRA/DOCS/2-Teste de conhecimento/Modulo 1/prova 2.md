---
# 📝 Prova 2 – Módulo 1: Estratégia e Arquitetura
---

1. AnyAirlines already has several point‑to‑point integrations between SaaS systems. They now want a more governed and reusable architecture. Which approach best aligns with MuleSoft recommendations?
   A. Add more scheduled jobs between systems as needed  
   B. Replace all integrations with a single monolithic API  
   C. Implement API‑led connectivity with System, Process and Experience APIs  
   D. Move all integrations into Salesforce Flow only  

2. NTO wants to expose product prices to multiple channels (web, mobile app, Salesforce). What is the most efficient way to design this according to API‑led principles?
   A. One Process API that all channels call directly  
   B. Separate System APIs for each channel  
   C. A shared Product System API plus dedicated Experience APIs per channel  
   D. Multiple duplicated APIs per consumer team  

3. A scenario describes a Composer flow calling an API that performs heavy aggregations across systems. Where should the complex business logic primarily reside?
   A. Inside the Composer formula editor  
   B. Inside the Salesforce Flow screen logic  
   C. Inside a Process API on Anypoint Platform  
   D. Inside the RPA bot actions  

4. A candidate suggests using RPA to automate a system that already exposes robust, secure REST APIs. Which statement best reflects MuleSoft best practice?
   A. Acceptable, because RPA is always simpler to configure  
   B. Not ideal; prefer API‑based integration first and reserve RPA for no‑API cases  
   C. Required, because exam scenarios always prefer RPA  
   D. Required, because APIs cannot be reused in other channels  

5. A retail customer wants near real‑time inventory updates between their ERP and Salesforce. Which tool combination best balances speed and maintainability?
   A. Only RPA bots reading ERP screens  
   B. Anypoint Platform System API for ERP plus Composer for light orchestration  
   C. Composer polling ERP database directly every second  
   D. Manual CSV uploads by users  

6. A scenario describes a complex multi‑step process where a human underwriter reviews cases over several days. Which component should coordinate long‑running steps while still leveraging APIs and RPA where needed?
   A. Single large RPA process with embedded decision logic  
   B. Salesforce Flow Orchestration with background and interactive steps  
   C. A large Composer flow with nested If/Else branches  
   D. A single Process API with many synchronous calls  

7. In a hyperautomation project, who is primarily responsible for promoting reuse of assets like APIs, RPA processes and fragments according to the C4E model?
   A. Only project managers  
   B. The Center for Enablement acting as an enablement and governance team  
   C. Individual developers working in isolation  
   D. External vendors only  

8. A question describes repeated failures in a hyperautomation chain whenever a legacy system is under heavy load. Which combination best addresses resilience at the integration layer?
   A. Remove logs to save processing time  
   B. Implement retries with exponential backoff and timeouts in the APIs  
   C. Move all logic to RPA bots to hide the problem  
   D. Increase Salesforce governor limits  

9. A company wants to test a new orchestration between Salesforce Flow and RPA while the final production credentials are not yet available. What is the safest test data strategy?
   A. Use real customer data in production systems  
   B. Use synthetic/mock data defined in API specifications  
   C. Export CSVs from production and mask only names  
   D. Duplicate production environment without any anonymization  

10. The exam presents four tool choices for a simple SaaS‑to‑SaaS integration with low volume and business admin ownership. Which one is most aligned with MuleSoft guidance?
    A. Anypoint Platform with fully custom APIs  
    B. MuleSoft Composer with out‑of‑the‑box connectors  
    C. RPA bots simulating all user clicks  
    D. Custom Java microservices on Kubernetes  

11. An architect proposes to centralize all error handling in the RPA layer. Why is this approach problematic for hyperautomation?
    A. APIs never fail, so this is unnecessary  
    B. Each layer (APIs, RPA, Flow, Composer) should handle its own technical concerns  
    C. RPA cannot log any errors  
    D. Composer has no way to react to failures  

12. A scenario mentions “avoiding duplicate login implementations across multiple teams”. Which platform capability directly supports this goal?
    A. Publishing shared RPA processes and API specs in Anypoint Exchange  
    B. Creating separate logins in each project for independence  
    C. Storing credentials in local text files  
    D. Embedding passwords into hard‑coded scripts  

13. NTO wants to quickly pilot a new customer journey using mocked APIs while backend systems are still under design. Which combination best supports this parallel development?
    A. RPA Recorder plus production database  
    B. Anypoint API Designer + Mocking Service consumed by Flow/Composer  
    C. Manual JSON files exchanged over email  
    D. Only Salesforce custom objects with no external connectivity  

14. A question describes a flow where Salesforce Screen Flows collect data from agents, which is then processed by RPA in a legacy system. Where should the primary user experience be built?
    A. In desktop RPA dialogs  
    B. In Salesforce Screen Flows integrated with APIs/RPA  
    C. In custom Java Swing applications  
    D. In raw database client tools  

15. An exam item shows multiple design options. Which is the strongest sign that one option is a “trap” rather than the recommended architecture?
    A. It emphasizes reuse of existing APIs and assets  
    B. It replaces three integrations with a single well‑designed Process API  
    C. It adds unnecessary components and ignores existing reusable services  
    D. It mentions C4E and governance practices
