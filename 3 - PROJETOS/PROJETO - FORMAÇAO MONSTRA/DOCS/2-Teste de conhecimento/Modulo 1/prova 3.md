---
# 📝 Prova 3 – Módulo 1: Decisão Técnica e Pegadinhas
---

1. AnyAirlines wants to expose flight status to partners, mobile apps and internal portals. What is the most efficient high‑level design?
   A. One monolithic API mixing database calls and UI logic  
   B. Separate, duplicated APIs for each consumer  
   C. System APIs for core data plus Process and Experience APIs for each channel  
   D. Only RPA bots reading from the reservation system  

2. A scenario offers the option to “rebuild a Customer System API from scratch” even though one already exists. Why is this typically wrong?
   A. Existing APIs cannot be reused  
   B. MuleSoft discourages versioning of APIs  
   C. It violates the principle of reuse and increases maintenance  
   D. System APIs are not allowed to expose customer data  

3. NTO needs a quick proof‑of‑concept integration from Salesforce to a legacy mainframe with no APIs. Which answer best reflects MuleSoft guidance?
   A. Start with MuleSoft RPA to simulate user interactions  
   B. Wait until a new REST API is built before doing anything  
   C. Use Composer directly against the database tables  
   D. Only manual rekeying is acceptable  

4. In an exam question, one option suggests performing complex aggregations in the Experience API, while another suggests doing it in the Process API. Which is more aligned with API‑led?
   A. Experience API, because it is closest to the user  
   B. Process API, because it centralizes business logic and orchestration  
   C. Both are equivalent according to MuleSoft  
   D. Neither; logic must always be in System APIs  

5. A flow uses RPA to fetch data from a legacy claims system and then sends the result to Salesforce. Where should retries and timeouts for unstable connectivity primarily be configured?
   A. Inside the Salesforce page layout  
   B. In the integration/API layer that receives or calls the RPA process  
   C. Inside the user’s browser  
   D. Nowhere; failures should be ignored  

6. A candidate chooses an option that adds Salesforce Flow Orchestration plus multiple new APIs when a simple synchronous API call from a Screen Flow would suffice. What kind of trap is this?
   A. Alternative technically impossible  
   B. Alternative that adds unnecessary complexity  
   C. Alternative that improves reuse  
   D. Alternative that follows minimal design  

7. An exam item describes a need for one‑time data migration from a CSV file into Salesforce. Which is the most appropriate integration approach?
   A. Full API‑led architecture with three layers  
   B. Complex RPA automation mimicking user input  
   C. Native Salesforce data import tools or simple integration  
   D. Building long‑running orchestrations with many stages  

8. A scenario gives two options: call a Process API that orchestrates multiple System APIs, or let Composer directly call each underlying system separately. Which is typically preferred?
   A. Composer calling all systems directly for flexibility  
   B. A Process API orchestrating System APIs, reused by Composer and other clients  
   C. Only RPA calling each system sequentially  
   D. Manual synchronization by business users  

9. A hyperautomation design includes Composer, RPA, Flow and multiple APIs. Which guiding principle helps keep this architecture maintainable?
   A. Push every responsibility to a single tool  
   B. Use each tool for the role it is strongest at and maximize reuse  
   C. Duplicate logic in each layer for redundancy  
   D. Prefer UI automation over APIs whenever possible  

10. An option claims that “creating separate APIs for each consuming application” improves reuse. Why is this misleading?
    A. MuleSoft does not support multiple APIs  
    B. True reuse comes from generic System/Process APIs with Experience APIs only when needed  
    C. Experience APIs cannot be consumer‑specific  
    D. Reuse is unrelated to API design  

11. A company wants to validate that their architecture still follows best practices one year after go‑live. Which practice best supports this?
    A. Ignoring C4E and allowing each team to evolve independently  
    B. Reviewing assets published in Anypoint Exchange and enforcing reuse policies  
    C. Rewriting all integrations annually  
    D. Migrating everything to RPA only  

12. In a multi‑choice question, two options look good, but one ignores API‑led layers and directly couples front‑end to databases. How should this influence the choice?
    A. Prefer the option that respects API‑led separation, even if more subtle  
    B. Prefer the option that bypasses layers for performance  
    C. Both are equally acceptable  
    D. Choose randomly if both seem possible  

13. A scenario describes a business user who must maintain a simple integration without developer support. Which integration tool is the exam most likely to expect?
    A. Anypoint Studio with complex DataWeave scripts  
    B. MuleSoft Composer with guided interface  
    C. Custom Java microservices  
    D. Low‑level HTTP clients  

14. NTO needs a fast temporary workaround using RPA while the proper APIs are being built. Which statement aligns with best practice?
    A. RPA should permanently replace API‑based integrations  
    B. RPA can act as a bridge, but long‑term strategy should be API‑led  
    C. RPA and APIs should never coexist  
    D. APIs are only for external consumers  

15. An exam option describes “calling the same System API from multiple Experience APIs and from RPA/Composer flows”. How should this be interpreted?
    A. As an anti‑pattern that must be avoided  
    B. As strong evidence of reuse and correct layering  
    C. As a sign that the System API is too generic  
    D. As a violation of security principles
