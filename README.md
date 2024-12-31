# my-local-ai-env
Descriptions of the hardware and software I have setup at my home office for running open-source, local-first, portable, multi-agent AI workflows.

I am building an AI agent/app to help people develop a career strategy and apply for jobs. The app doesn’t need an internet connection, so I want to focus on local desktop apps for Mac, Windows, and Linux. I will likely use Rust and TypeScript for languages. I want to keep focused on local-first stacks, so I won’t be deploying this to multi-tier cloud environments, which lets me keep it hella simple and private/secure. 

## Hardware
### Alienware Aurora 16
https://www.dell.com/en-us/shop/desktop-computers/alienware-aurora-r16-gaming-desktop/spd/alienware-aurora-r16-desktop
https://www.nvidia.com/en-us/geforce/graphics-cards/40-series/rtx-4090/

## Software
I’m obsessed with open source, self-hosted, local first, multi-agent workflows. This starter kit is how I’ll prototype my next project: https://github.com/n8n-io/self-hosted-ai-starter-kit. I want to build open AI agents to help people find work and balance out all the corporate AI recruiting automation. The tech stack is centered around libraries like Ollama, LangChain, n8n, and Neo4j.

I’m focused on getting people off big tech cloud providers for benefits related to cost, privacy, security, intellectual property, control, and simplicity. The only hosting providers I plan on using are highly principled companies like Hugging Face, Mistral, Together.ai, and http://Storj.io when local computing or storage doesn’t fit the use case.

### Software Infrastructure
https://ubuntu.com/desktop/wsl
https://learn.microsoft.com/en-us/windows/wsl/install
Docker: This is your containerization platform that packages all AI components into manageable, isolated environments. It will help us run all the AI tools with a single command. https://www.docker.com/products/docker-desktop/
FastAPI

### Data Infrastructure
https://neo4j.com/download/neo4j-desktop
https://neo4j.com/labs/genai-ecosystem/llm-graph-builder/
Postgres: This tool stores all data and logs, acting as a memory buffer for the n8n framework.
Qdrant: A vector database and search engine that makes AI-generated content searchable and manageable.
Storj for object storage and backup. http://storj.io/

### AI Infrastructure
Ollama: An AI model manager that enables you to run any open-source large language model locally with minimal hardware requirements. https://ollama.com/
https://www.nvidia.com/en-gb/deep-learning-ai/solutions/data-science/
https://github.com/NVIDIA/data-science-stack
LangChain for orchestration
n8n: A workflow automation framework that allows you to build AI workflows using a drag-and-drop interface. It requires no coding knowledge, making it ideal for non-technical individuals. https://n8n.io/integrations/

### Machine Learning Models
https://huggingface.co/NousResearch/Hermes-3-Llama-3.2-3B
mixtral 8x7B
Mistral 7B

### AI Playgrounds
https://github.com/n8n-io/self-hosted-ai-starter-kit
https://neo4j.com/developer-blog/langchain-neo4j-starter-kit/

### Conversational User Interfaces
https://lmstudio.ai/
https://openwebui.com/

### Front-End Development
https://v2.tauri.app/
https://v2.tauri.app/start/frontend/sveltekit/

## Documentation
### Technical Docs
https://documentation.ubuntu.com/wsl/en/latest/
https://docs.n8n.io/hosting/architecture/overview/

### Tutorials
https://medium.com/@Tanzim/how-to-run-ollama-in-windows-via-wsl-8ace765cee12
https://blogs.nvidia.com/blog/ai-decoded-lm-studio/
https://www.datacamp.com/tutorial/local-ai
https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Frameworks_libraries/Svelte_getting_started
https://electric-sql.com/blog/2024/02/05/local-first-ai-with-tauri-postgres-pgvector-llama
https://neo4j.com/blog/graphrag-manifesto/
https://neo4j.com/developer/genai-ecosystem/ai-for-customer-experiences/

## Install Log
### PowerShell

### Ubuntu
curl https://ollama.ai/install.sh | sh
ollama run mistral

git clone https://github.com/NVIDIA/data-science-stack
cd data-science-stack
./data-science-stack setup-system
