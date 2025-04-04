# my-local-ai-env
Descriptions of the hardware and software I have setup at my home office for running open-source, local-first, portable, multi-agent AI workflows.

I am building an AI agent/app to help people develop a career strategy and apply for jobs. The app doesn’t need an internet connection, so I want to focus on local desktop apps for Mac, Windows, and Linux. I will likely use Rust and TypeScript for languages. I want to keep focused on local-first stacks, so I won’t be deploying this to multi-tier cloud environments, which lets me keep it hella simple and private/secure. 

## Hardware
### Alienware Aurora 16
https://www.dell.com/en-us/shop/desktop-computers/alienware-aurora-r16-gaming-desktop/spd/alienware-aurora-r16-desktop

https://www.nvidia.com/en-us/geforce/graphics-cards/40-series/rtx-4090/

https://www.intel.com/content/www/us/en/products/details/processors/core/i9.html

## Software
I’m obsessed with open source, self-hosted, local first, multi-agent workflows. This starter kit is how I’ll prototype my next project: https://github.com/n8n-io/self-hosted-ai-starter-kit. I want to build open AI agents to help people find work and balance out all the corporate AI recruiting automation. The tech stack is centered around libraries like Ollama, LangChain, n8n, and Neo4j.

I’m focused on getting people off big tech cloud providers for benefits related to cost, privacy, security, intellectual property, control, and simplicity. The only hosting providers I plan on using are highly principled companies like Hugging Face, Mistral, Together.ai, and http://Storj.io when local computing or storage doesn’t fit the use case.

### Software Infrastructure
https://ubuntu.com/desktop/wsl

https://learn.microsoft.com/en-us/windows/wsl/install

Docker: This is your containerization platform that packages all AI components into manageable, isolated environments. It will help us run all the AI tools with a single command. https://www.docker.com/products/docker-desktop/

https://docs.docker.com/desktop/features/wsl/

https://git-scm.com/downloads/win

FastAPI

### Data Infrastructure
https://neo4j.com/download/neo4j-desktop

https://neo4j.com/labs/genai-ecosystem/llm-graph-builder/

Postgres: This tool stores all data and logs, acting as a memory buffer for the n8n framework.

Qdrant: A vector database and search engine that makes AI-generated content searchable and manageable.

Storj for object storage and backup. http://storj.io/

### AI Infrastructure
NVIDIA CUDA toolkit for WSL 2 on Ubuntu

Ollama: An AI model manager that enables you to run any open-source large language model locally with minimal hardware requirements. https://ollama.com/

https://www.nvidia.com/en-gb/deep-learning-ai/solutions/data-science/

https://github.com/NVIDIA/data-science-stack

LangChain for orchestration

n8n: A workflow automation framework that allows you to build AI workflows using a drag-and-drop interface. It requires no coding knowledge, making it ideal for non-technical individuals. https://n8n.io/integrations/

### Machine Learning Models
Mistral AI and NVIDIA Unveil Mistral NeMo 12B, a Cutting-Edge Enterprise AI Model: Designed to fit on the memory of a single NVIDIA L40S, NVIDIA GeForce RTX 4090 or NVIDIA RTX 4500 GPU, the Mistral NeMo NIM offers high efficiency, low compute cost, and enhanced security and privacy. https://blogs.nvidia.com/blog/mistral-nvidia-ai-model/

https://huggingface.co/docs/transformers/installation

PyTorch installation instructions.

TensorFlow 2.0 installation instructions.

Flax installation instructions.

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
https://documentation.ubuntu.com/wsl/en/latest/tutorials/gpu-cuda/

https://documentation.ubuntu.com/wsl/en/latest/tutorials/data-science-and-engineering/

https://medium.com/@Tanzim/how-to-run-ollama-in-windows-via-wsl-8ace765cee12

https://blogs.nvidia.com/blog/ai-decoded-lm-studio/

https://www.datacamp.com/tutorial/local-ai

https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Frameworks_libraries/Svelte_getting_started

https://electric-sql.com/blog/2024/02/05/local-first-ai-with-tauri-postgres-pgvector-llama

https://neo4j.com/blog/graphrag-manifesto/

https://neo4j.com/developer/genai-ecosystem/ai-for-customer-experiences/

https://www.reddit.com/r/ollama/comments/1cpo6nb/lan_configuration_for_open_webui/

### Troubleshooting
https://www.pdq.com/blog/what-is-the-powershell-equivalent-of-ipconfig/

## Install Log
### In Windows PowerShell Terminal
Developers can access the power of both Windows and Linux at the same time on a Windows machine. The Windows Subsystem for Linux (WSL) lets developers install a Linux distribution (such as Ubuntu, OpenSUSE, Kali, Debian, Arch Linux, etc) and use Linux applications, utilities, and Bash command-line tools directly on Windows, unmodified, without the overhead of a traditional virtual machine or dualboot setup.

https://learn.microsoft.com/en-us/windows/wsl/install

If you wish to utilize Open WebUI with Ollama included or CUDA acceleration, we recommend utilizing our official images tagged with either :cuda or :ollama. To enable CUDA, you must install the Nvidia CUDA container toolkit on your Linux/WSL system.

https://docs.nvidia.com/dgx/nvidia-container-runtime-upgrade/

    Linux applications can run as is in WSL 2. WSL 2 is characteristically a VM with a Linux WSL Kernel in it that provides full compatibility with mainstream Linux kernel allowing support for native Linux applications including popular Linux distros.
    Faster file system support and that’s more performant.
    WSL 2 is tightly integrated with the Microsoft Windows operating system, which allows it to run Linux applications alongside and even interop with other Windows desktop and modern store apps.
    
With NVIDIA CUDA support for WSL 2, developers can leverage NVIDIA GPU accelerated computing technology for data science, machine learning and inference on Windows through WSL. GPU acceleration also serves to bring down the performance overhead of running an application inside a WSL like environment close to near-native by being able to pipeline more parallel work on the GPU with less CPU intervention.
![Figure 1. Illustration of the possibilities with NVIDIA CUDA software stack on WSL 2](https://docs.nvidia.com/cuda/wsl-user-guide/_images/wsl-launch-upt-0625-rz.png)

https://docs.nvidia.com/cuda/wsl-user-guide/index.html

For example, when storing your WSL project files:

    Use the Linux file system root directory: \\wsl$\<DistroName>\home\<UserName>\Project
    Not the Windows file system root directory: C:\Users\<UserName>\Project or /mnt/c/Users/<UserName>/Project$

![alt text](https://learn.microsoft.com/en-us/windows/wsl/media/windows-file-explorer.png)

The NVIDIA Container Toolkit allows users to build and run GPU accelerated Docker containers. The toolkit includes a container runtime library and utilities to configure containers to leverage NVIDIA GPUs automatically. Complete documentation and frequently asked questions are available on the repository wiki.
![alt text](dg-docker-01.png)
https://docs.nvidia.com/ai-enterprise/deployment/vmware/latest/docker.html

The latest NVIDIA Windows GPU Driver will fully support WSL 2. With CUDA support in the driver, existing applications (compiled elsewhere on a Linux system for the same target GPU) can run unmodified within the WSL environment.

### In Ubuntu WSL2 Terminal

To compile new CUDA applications, a CUDA Toolkit for Linux x86 is needed. CUDA Toolkit support for WSL is still in preview stage as developer tools such as profilers are not available yet. However, CUDA application development is fully supported in the WSL2 environment, as a result, users should be able to compile new CUDA Linux applications with the latest CUDA Toolkit for x86 Linux.

Option 1: Installation of Linux x86 CUDA Toolkit using WSL-Ubuntu Package - Recommended

The CUDA WSL-Ubuntu local installer does not contain the NVIDIA Linux GPU driver, so by following the steps on the CUDA download page for WSL-Ubuntu, you will be able to get just the CUDA toolkit installed on WSL.

```
wget https://developer.download.nvidia.com/compute/cuda/repos/wsl-ubuntu/x86_64/cuda-wsl-ubuntu.pin
sudo mv cuda-wsl-ubuntu.pin /etc/apt/preferences.d/cuda-repository-pin-600
wget https://developer.download.nvidia.com/compute/cuda/12.8.1/local_installers/cuda-repo-wsl-ubuntu-12-8-local_12.8.1-1_amd64.deb
sudo dpkg -i cuda-repo-wsl-ubuntu-12-8-local_12.8.1-1_amd64.deb
sudo cp /var/cuda-repo-wsl-ubuntu-12-8-local/cuda-*-keyring.gpg /usr/share/keyrings/
sudo apt-get update
sudo apt-get -y install cuda-toolkit-12-8
```

https://developer.nvidia.com/cuda-downloads?target_os=Linux&target_arch=x86_64&Distribution=WSL-Ubuntu&target_version=2.0&target_type=deb_local

Install using the apt repository

Before you install Docker Engine for the first time on a new host machine, you need to set up the Docker apt repository. Afterward, you can install and update Docker from the repository.

    Set up Docker's apt repository.
```

# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "${UBUNTU_CODENAME:-$VERSION_CODENAME}") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```
Install the Docker packages. To install the latest version, run:
```
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

Configure the production repository:
```
curl -fsSL https://nvidia.github.io/libnvidia-container/gpgkey | sudo gpg --dearmor -o /usr/share/keyrings/nvidia-container-toolkit-keyring.gpg \
  && curl -s -L https://nvidia.github.io/libnvidia-container/stable/deb/nvidia-container-toolkit.list | \
    sed 's#deb https://#deb [signed-by=/usr/share/keyrings/nvidia-container-toolkit-keyring.gpg] https://#g' | \
    sudo tee /etc/apt/sources.list.d/nvidia-container-toolkit.list
```


Update the packages list from the repository:
```
sudo apt-get update
```

Install the NVIDIA Container Toolkit packages:
```
sudo apt-get install -y nvidia-container-toolkit
```

Prerequisites

    You installed a supported container engine (Docker, Containerd, CRI-O, Podman).

    You installed the NVIDIA Container Toolkit.

Configuring Docker

Configure the container runtime by using the nvidia-ctk command:
```
sudo nvidia-ctk runtime configure --runtime=docker
```

The nvidia-ctk command modifies the /etc/docker/daemon.json file on the host. The file is updated so that Docker can use the NVIDIA Container Runtime.

Restart the Docker daemon:
```
sudo systemctl restart docker
```

https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/install-guide.html#installing-the-nvidia-container-toolkit



Follow this step-by-step guide to Get started using Visual Studio Code with WSL, which includes installing the Remote Development extension pack. This extension enables you to run WSL, SSH, or a development container for editing and debugging with the full set of Visual Studio Code features. Quickly swap between different, separate development environments and make updates without worrying about impacting your local machine.

Once VS Code is installed and set up, you can open your WSL project with a VS Code remote server by entering: code .

https://learn.microsoft.com/en-us/windows/wsl/tutorials/wsl-vscode

Follow this step-by-step guide to Get started using Git on WSL and connect your project to the Git version control system, along with using the credential manager for authentication, using Git Ignore files, understanding Git line endings, and using the Git commands built-in to VS Code.

![alt text](https://learn.microsoft.com/en-us/windows/wsl/media/git-versions.gif)

https://learn.microsoft.com/en-us/windows/wsl/tutorials/wsl-git

Follow this step-by-step guide to Get started with Docker remote containers on WSL 2 and connect your project to a remote development container with Docker Desktop for Windows.

https://learn.microsoft.com/en-us/windows/wsl/tutorials/wsl-containers

Follow this step-by-step guide to set up GPU accelerated machine learning training in WSL and leverage your computer's GPU (graphics processing unit) to accelerate performance heavy workloads.

https://learn.microsoft.com/en-us/windows/wsl/tutorials/gpu-compute



To get up and running with large language models:
```
curl -fsSL https://ollama.com/install.sh | sh
```
Or
```
curl https://ollama.ai/install.sh | sh
ollama run mistral-nemo
```

https://github.com/ollama/ollama

To run Open WebUI with Nvidia GPU support, use this command:
```
docker run -d -p 3000:8080 --gpus all --add-host=host.docker.internal:host-gateway -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:cuda
```
https://github.com/open-webui/open-webui


```
git clone https://github.com/NVIDIA/data-science-stack
cd data-science-stack
./data-science-stack setup-system
```

```
C:\Users\paulp> sudo netsh interface portproxy add v4tov4 listenport=8080 listenaddress=0.0.0.0 connectport=8080 connectaddress=192.168.1.254
```