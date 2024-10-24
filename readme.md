# TeraBot Airtel

TeraBot Airtel is an intelligent chatbot application built using FastAPI for the backend and React for the frontend. The chatbot allows users to interact with it for various queries, including SIM swap requests and recharge plan inquiries. 

## Demo

Watch the demo of the Airtel chatbot in action:

[![Watch the Demo](https://img.youtube.com/vi/dQw4w9WgXcQ/0.jpg)](https://raw.githubusercontent.com/AnandPTi/TeraBotAirtel/1792d288b97e049e0fcc41f6e4b2e2eca29b3f1e/Demo.webm)


## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Environment Variables](#environment-variables)
- [Backend Setup](#backend-setup)
- [Frontend Setup](#frontend-setup)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Requirements](#requirements)
- [Contributing](#contributing)
- [License](#license)



## Features

- **Chat Interface**: User-friendly chat interface for seamless interaction.
- **SIM Swap Requests**: Users can request a SIM swap by providing their details.
- **Recharge Plans**: Inquire about various recharge plans and select one for further processing.
- **Session Management**: Keeps track of user sessions to manage conversations effectively.
- **CORS Support**: Enables communication between the frontend and backend.

## Installation

To set up the project locally, follow these steps:

1. **Clone the repository:**

   ```bash
   git clone <repository-url>
   cd <project-directory>
   ```

2. **Set up the environment:**

   Create a `.env` file in the root of your project and add your API keys:

   ```plaintext
   OPENAI_API_KEY=sk-proj-***************************************************************
   PINECONE_API_KEY=pcsk_2zxSyP_**********************************************************
   ```

## Backend Setup

1. **Navigate to the backend directory:**

   ```bash
   cd Backend
   ```

2. **Install dependencies:**

   Create a virtual environment and install the required packages:

   ```bash
   python -m venv botenv
   source botenv/bin/activate  # On Windows use `botenv\Scripts\activate`
   pip install -r requirements.txt
   ```

3. **Run the FastAPI server:**

   ```bash
   python server.py
   ```

   The server will start on `http://localhost:8000`.

## Frontend Setup

1. **Navigate to the frontend directory:**

   ```bash
   cd Frontend
   ```

2. **Install dependencies:**

   Make sure you have Node.js installed. Then run:

   ```bash
   npm install
   ```

3. **Run the React application:**

   ```bash
   npm start
   ```

   The application will start on `http://localhost:3000`.

## Usage

Once both the backend and frontend are running:

1. Open your browser and navigate to `http://localhost:3000`.
2. Start interacting with TeraBot by entering your queries into the chat interface.

## API Endpoints

### POST /chat

This endpoint handles chat messages and responses.

- **Request Body:**

   ```json
   {
     "message": "Your message here",
     "user_id": "optional_user_id"
   }
   ```

- **Response:**

   ```json
   {
     "response": "Bot's response here"
   }
   ```

## Requirements

The project uses the following libraries and their specified versions for the backend:

```plaintext
aiohappyeyeballs==2.4.3
aiohttp==3.9.5
aiosignal==1.3.1
annotated-types==0.7.0
anyio==4.6.2.post1
attrs==24.2.0
azure-ai-ml==1.21.1
azure-common==1.1.28
azure-core==1.31.0
azure-identity==1.19.0
azure-mgmt-core==1.4.0
azure-storage-blob==12.23.1
azure-storage-file-datalake==12.17.0
azure-storage-file-share==12.19.0
beautifulsoup4==4.12.3
cachetools==5.5.0
certifi==2024.8.30
cffi==1.17.1
charset-normalizer==3.4.0
click==8.1.7
colorama==0.4.6
cryptography==43.0.3
dataclasses-json==0.6.7
distro==1.9.0
faiss-cpu==1.9.0
fastapi==0.115.3
frozenlist==1.5.0
gitdb==4.0.11
GitPython==3.1.43
google-api-core==2.21.0
google-auth==2.35.0
googleapis-common-protos==1.65.0
greenlet==3.1.1
gritql==0.1.5
h11==0.14.0
httpcore==1.0.6
httpx==0.27.2
httpx-sse==0.4.0
idna==3.10
isodate==0.7.2
jiter==0.6.1
jsonpatch==1.33
jsonpointer==3.0.0
jsonschema==4.23.0
jsonschema-specifications==2024.10.1
langchain==0.3.4
langchain-cli==0.0.31
langchain-community==0.3.3
langchain-core==0.3.12
langchain-openai==0.2.3
langchain-pinecone==0.2.0
langchain-text-splitters==0.3.0
langgraph==0.2.39
langgraph-checkpoint==2.0.1
langgraph-sdk==0.1.33
langserve==0.3.0
langsmith==0.1.137
markdown-it-py==3.0.0
marshmallow==3.23.0
mdurl==0.1.2
msal==1.31.0
msal-extensions==1.2.0
msgpack==1.1.0
msrest==0.7.1
multidict==6.1.0
mypy-extensions==1.0.0
numpy==1.26.4
oauthlib==3.2.2
openai==1.52.1
opencensus==0.11.4
opencensus-context==0.1.3
opencensus-ext-azure==1.1.13
opencensus-ext-logging==0.1.1
orjson==3.10.10
packaging==24.1
pinecone-client==5.0.1
pinecone-plugin-inference==1.1.0
pinecone-plugin-interface==0.0.7
portalocker==2.10.1
propcache==0.2.0
proto-plus==1.25.0
protobuf==5.28.3
psutil==6.1.0
pyasn1==0.6.1
pyasn1_modules==0.4.1
pycparser==2.22
pydantic==2.9.2
pydantic-settings==2.6.0
pydantic_core==2.23.4
pydash==8.0.3
Pygments==2.18.0
PyJWT==2.9.0
python-dateutil==2.9.0.post0
python-dotenv==1.0.1
PyYAML==6.0.2
referencing==0.35.1
regex==2024.9.11
requests==2.32.3
requests-oauthlib==2.0.0
requests-toolbelt==1.0.0
rich==13.9.3
rpds-py==0.20.0
rsa==4.9
shellingham==1.5.4
six==1.16.0
smmap==5.0.1
sniffio==1.3.1
soupsieve==2.6
SQLAlchemy==2.0.36
sse-starlette==1.8.2
starlette==0.41.0
strictyaml==1.7.3
tenacity==9.0.0
tiktoken==0.8.0
tomlkit==0.12.5
tqdm==4.66.5
typer==0.9.4
typing-inspect==0.9.0
typing_extensions==4.12.2
urllib3==2.2.3
uvicorn==0.23.2
yarl==1.16.0

```


For the frontend, ensure you have the required React packages, which will be installed when you run `npm install`.

# Extras

## Chatbot Overview

This project features an AI-powered chatbot designed to assist users with various Airtel-related queries. The chatbot intelligently routes user inquiries to the appropriate workflows, ensuring quick and accurate responses.

## How It Works

The chatbot utilizes a combination of advanced machine learning models and vector stores to process user questions. It follows a structured approach to determine the most relevant datasource for each inquiry based on predefined routing guidelines.

### Key Components:

1. **Routing System**: 
   - The chatbot uses a structured output model to route inquiries based on their context. For example, general Airtel-related questions are directed to a knowledge-based model, while SIM swap queries trigger a specific workflow.
   
2. **State Graph**:
   - Implemented using **LangGraph**, the state graph allows for the management of different workflow nodes (e.g., handling basic inquiries, retrieving knowledge base documents, and managing SIM swap requests). Each node corresponds to a specific functionality.

3. **Vector Store**:
   - The chatbot integrates with **Pinecone** for efficient retrieval of relevant documents. When a user asks a question, the system performs a similarity search to find the most applicable information from the vector store.

4. **Language Model**:
   - It leverages **LangChain** and **OpenAI** models (e.g., GPT-4) to generate human-like responses based on user queries and retrieved information. 

### Workflow Process:

- **User Input**: Users interact with the chatbot by typing in their queries.
- **Routing Logic**: The system analyzes the input and routes it to the corresponding workflow using a predefined prompt.
- **Document Retrieval**: If the query pertains to Airtel's services, the chatbot retrieves relevant documents from the vector store and formulates a response.
- **Response Generation**: The final response is generated by the OpenAI language model and returned to the user.

### Example Queries Handled:
- General inquiries about Airtel services.
- Requests for SIM swap procedures.
- Information about current recharge plans.

## Tools and Technologies Used:
- **LangChain**: For integrating language models and creating a structured query-routing system.
- **LangGraph**: To manage the stateful workflows within the chatbot.
- **Pinecone**: For efficient document retrieval based on user queries.
- **OpenAI**: To generate responses using advanced language models.

This chatbot aims to provide a seamless user experience by intelligently understanding and responding to user inquiries about Airtel services.


## License

This project is licensed under the MIT License. See the LICENSE file for details.

