## Open AI CODEX Prompts to generate a prototype of an Agentic Workflow

### Technology Stack
1. Client (UI)
   - This part will be PhP with apeche webserver
2. Server (The REST Web services and Agentic Workflows)
   - This will use python with following packages
     - FastAPI
     - MySQL Database
     - SQL Alchemy
     - Pydantic
     - Typing
     - LangChain
    
### The frontend website 
We will build an MVC based structure for a website that has a home page with two options 
   1. Meet the AI-Doctor
   2. Provide Feedback.
   3. Admin Page
      - This page will be accessible with a fixed user name and password (for simplicity).
      - It will enable the admin to run sentiment analysis for feedbacks that have been received today
      - get data to generate report and plots.
      - The entire activity will be built using two prompts
         - The first prompt will only set up the required environment
         - In the second phase the actual pages will be createdwhich we will do with the second prompt.
