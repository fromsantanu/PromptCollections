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
    
### The Frontend Website 

##### Here we will build an MVC based structure for a website that has a home page with two options 
   1. Meet the AI-Doctor
   2. Provide Feedback.
   3. Admin Page
      - This page will be accessible with a fixed user name and password (for simplicity).
      - It will enable the admin to run sentiment analysis for feedbacks that have been received today
      - get data to generate report and plots.
   4. The entire activity will be built using two prompts
      - The first prompt will only set up the required environment.  [**Refer to the first prompt here**](#)
      - In the second phase the actual pages will be createdwhich we will do with the second prompt. [**Refer to the second prompt here**](#)

### The Backend 

##### The Backend will contain the following services and workflows 

1. A POST service to collect patients Unique ID, name, age, email id, complaints, vitals informations etc.
and trigger a workflow in langchain to generate a general advice on test prescription and home based treatment  based on his complaint or an advice to immediate visit of health center in case it requires doctors atention. The treatment advice will be recorded in a MySQL database and also email will be sent to the patient.

2) A POST service for recording patients feedback. Patient will provide his unique id, name, gender, age, religion, review comment on the faciity.

3) A GET service that will trigger a workflow in langchain to do a sentiment analysis updating two fields in the feedback record of each of the above rows
   1. Sentiment (column).
   2. Percentage (column). This workflow will also send json data necessary to generate plots. This API will be triggered by a button in admin screen in the Php MVC system that we discussed earlier.  

[**Refer to the detailed prompt here**](#)

 
