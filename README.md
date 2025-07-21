# 🚀 Azure AI Foundry E2E Laboratory

[![Azure AI Foundry](https://img.shields.io/badge/Azure%20AI-Foundry-blue?style=for-the-badge&logo=microsoft)](https://ai.azure.com)
[![Python](https://img.shields.io/badge/Python-3.10+-green?style=for-the-badge&logo=python)](https://python.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-Lab-orange?style=for-the-badge&logo=jupyter)](https://jupyter.org)

**End-to-End AI Development Laboratory by Kapil Dhanger**

*Master Azure AI Foundry through hands-on experimentation and real-world applications*

---

🎯 [Getting Started](#-getting-started) • 📚 [Learning Path](#-learning-path) • 🔧 [Setup Guide](#-environment-setup) • 🛠️ [Troubleshooting](#-troubleshooting--support)

---

## 🎯 Mission Statement

This comprehensive laboratory transforms you from an AI enthusiast into an Azure AI Foundry expert. Through progressive, hands-on modules, you'll master:

🔬 **Core AI Engineering**
- Advanced model deployment strategies and optimization techniques
- Production-ready authentication and security implementation  
- Scalable project architecture and configuration management

🤖 **Intelligent Agent Development**
- Multi-modal AI agents with specialized capabilities
- Advanced RAG (Retrieval-Augmented Generation) implementations
- Real-time decision-making systems and automated workflows

🏗️ **Enterprise-Grade Solutions**
- End-to-end AI application development with modern frameworks
- Multi-agent orchestration and coordination patterns
- Quality assurance through comprehensive evaluation and monitoring

> **🎓 Laboratory Format**: 4-5 hour intensive hands-on experience  
> **🎯 Target Audience**: Developers, AI practitioners, and solution architects  
> **💡 Learning Approach**: Progressive complexity with real-world applications

---

## 📁 Repository Structure

```
ai-foundry-e2e-lab/
├── 📚 initial-setup/           # Start here - Authentication & environment setup
├── 💬 chat-rag/               # Chat completion and RAG fundamentals
├── 🤖 agents/                 # AI Agents development and tools
├── 🔄 multi-agent/            # Multi-agent systems and orchestration
├── 🏗️ frameworks/             # Advanced frameworks (Semantic Kernel, AutoGen)
├── ⚡ azure-functions/         # Serverless integration patterns
├── 📊 observalibility/         # Monitoring, evaluation, and quality assurance

```

---

## 🚀 Getting Started

### Step 1: Repository Setup

```powershell
# Clone the laboratory repository
git clone https://github.com/dhangerkapil/ai-foundry-e2e-lab.git
cd ai-foundry-e2e-lab

# Verify Python version
python --version  # Should be 3.10 or higher
```

### Step 2: Python Environment Configuration

**Option A: Using UV (Recommended - Fastest)**
```powershell
# Install UV package manager for Windows PowerShell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"

# Create and activate virtual environment
uv venv
.\.venv\Scripts\Activate.ps1
```

**Option B: Using Standard venv**
```powershell
# Create and activate virtual environment
python -m venv .venv
.\.venv\Scripts\activate
```

### Step 3: Install Dependencies

```powershell
# Install core dependencies
pip install -r requirements.txt

# Register Jupyter kernel
python -m ipykernel install --user --name=ai-foundry-lab --display-name="AI Foundry Lab"
```

### Step 4: Azure AI Foundry Setup

1. **Create Azure AI Foundry Project**
   - Navigate to [Azure AI Foundry Portal](https://ai.azure.com)
   - Create a new project with Standard pricing tier
   - Choose region based on model availability (East US recommended)

2. **Deploy Required Models**
   
   | Model Type | Recommended Models | Purpose |
   |------------|-------------------|---------|
   | **Chat/Completion** | `gpt-4o`, `gpt-4o-mini` | Primary reasoning & conversation |
   | **Embeddings** | `text-embedding-3-large` | Vector search & RAG |
   | **Specialized** | `phi-4`, `deepseek-r1` | Domain-specific tasks |

3. **Configure Environment Variables**
   ```env
   PROJECT_CONNECTION_STRING=your-project-connection-string
   MODEL_DEPLOYMENT_NAME=your-primary-model-deployment-name
   EMBEDDING_MODEL_DEPLOYMENT_NAME=your-embedding-model-deployment-name
   TENANT_ID=your-azure-tenant-id
   ```

---

## 📚 Learning Path

Follow this structured learning path to master Azure AI Foundry:

### 🎯 Phase 1: Foundation (Start Here)
**Location:** `initial-setup/`

| Notebook | Description |
|----------|-------------|
| 🔐 [Authentication](initial-setup/1-authentication.ipynb) | Azure credential setup and security |
| ⚙️ [Environment Setup](initial-setup/2-environment_setup.ipynb) | Development environment configuration |
| 🚀 [Quick Start](initial-setup/3-quick_start.ipynb) | First AI model interaction |

### 💬 Phase 2: Chat & RAG Fundamentals
**Location:** `chat-rag/`

| Notebook | Description |
|----------|-------------|
| 💬 [Basic Chat Completion](chat-rag/1-basic-chat-completion.ipynb) | Foundation models and prompting |
| 🔍 [Embeddings](chat-rag/2-embeddings.ipynb) | Vector representations and similarity |
| 📚 [Basic RAG](chat-rag/3-basic-rag.ipynb) | Retrieval-Augmented Generation |
| 🧠 [Phi-4](chat-rag/4-phi-4.ipynb) | Microsoft's reasoning model |
| 🤖 [DeepSeek R1](chat-rag/5-deep-seek-r1.ipynb) | Advanced reasoning capabilities |

### 🤖 Phase 3: AI Agents Development  
**Location:** `agents/`

| Notebook | Description |
|----------|-------------|
| 🤖 [Agent Basics](agents/1-basics.ipynb) | Fundamental agent concepts |
| 💻 [Code Interpreter](agents/2-code_interpreter.ipynb) | Code execution capabilities |
| 📄 [File Search](agents/3-file-search.ipynb) | Document processing |
| 🌐 [Bing Grounding](agents/4-bing_grounding.ipynb) | Web search integration |
| 🔍 [Agents + AI Search](agents/5-agents-aisearch.ipynb) | Enterprise search integration |
| ⚡ [Agents + Azure Functions](agents/6-agents-az-functions.ipynb) | Serverless integration |

### 🔄 Phase 4: Multi-Agent Systems
**Location:** `multi-agent/`

| Notebook | Description |
|----------|-------------|
| 👥 [Multi-Agent Solution](multi-agent/multi-agent-solution.ipynb) | Collaborative AI systems |
| 📊 [Multi-Agent with Tracing](multi-agent/multi-agent-solution-with-tracing.ipynb) | Advanced monitoring |

### 🏗️ Phase 5: Advanced Frameworks
**Location:** `frameworks/`

| Notebook | Description |
|----------|-------------|
| 🔧 [RAG + Semantic Kernel + Agents](frameworks/1-rag-sk-agents-aisearch.ipynb) | Microsoft's orchestration framework |
| 🤖 [AutoGen Multi-Agent RAG](frameworks/2-autogen-multi-agent-rag.ipynb) | Automated agent generation |
| ❤️ [AutoGen Personalized Analytics](frameworks/3-autogen-personalized-heart-rate.ipynb) | Health domain specialization |

### 📊 Phase 6: Quality & Operations
**Location:** `observalibility/`

| Notebook | Description |
|----------|-------------|
| 👁️ [Observability](observalibility/1-Observability.ipynb) | Monitoring and telemetry |
| 📈 [Evaluation](observalibility/2-evaluation.ipynb) | Quality assessment and benchmarking |

### ⚡ Phase 7: Serverless Integration
**Location:** `azure-functions/`

Explore serverless AI patterns with Azure Functions integration for scalable, event-driven AI applications.

---

## 🔧 Environment Setup

### 📋 System Requirements

**Essential Components:**
- 🐍 [Python 3.10+](https://www.python.org/downloads/) - Latest stable version
- ☁️ [Azure Subscription](https://ai.azure.com) - Active subscription with Azure AI Foundry access
- 💻 [Visual Studio Code](https://code.visualstudio.com/) - Recommended development environment
- 🛠️ [Azure CLI](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli) - For resource management
- 📦 [Git](https://git-scm.com/downloads) - Version control

**Knowledge Prerequisites:**
- ✅ Intermediate Python programming skills
- ✅ Basic understanding of machine learning concepts
- ✅ Familiarity with REST APIs and web services
- ✅ Experience with Azure services (recommended)

### 🔧 Development Environment Setup

**Visual Studio Code (Recommended)**
```powershell
# Install required extensions
code --install-extension ms-python.python
code --install-extension ms-toolsai.jupyter
```

**Alternative: JupyterLab**
```powershell
# Launch JupyterLab
jupyter lab
```

---

## 🛠️ Troubleshooting & Support

### ⚡ Common Issues & Solutions

**Kernel Issues in VS Code:**
```powershell
# Refresh kernel registration
python -m ipykernel install --user --name=ai-foundry-lab --display-name="AI Foundry Lab"
# Reload VS Code: Ctrl+Shift+P → "Developer: Reload Window"
```

**Environment Activation Problems:**
```powershell
# Set PowerShell execution policy
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser

# Verify virtual environment
python -c "import sys; print(sys.executable)"
```

**Azure Authentication Issues:**
```powershell
# Clear cached credentials and re-login
az account clear
az login --tenant YOUR_TENANT_ID
az account show
```

### 📚 Additional Resources

- 📖 [Azure AI Foundry Documentation](https://learn.microsoft.com/en-us/azure/ai-foundry/)
- 🎥 [Video Tutorials](https://learn.microsoft.com/en-us/shows/ai-show/)
- 💡 [Best Practices Guide](https://learn.microsoft.com/en-us/azure/ai-services/responsible-use-of-ai-overview)
- 🔍 [GitHub Issues](https://github.com/dhangerkapil/ai-foundry-e2e-lab/issues) - Report bugs or request features

---

## 🤝 Community & Contributions

### 🌟 Ways to Contribute
- 📝 **Documentation**: Improve clarity and add examples
- 🐛 **Bug Reports**: Help us identify and fix issues  
- 💡 **Feature Requests**: Suggest new capabilities and improvements
- 🔄 **Pull Requests**: Contribute code and enhancements

### 📋 Contribution Guidelines
Please review our [Contributing Guide](CONTRIBUTING.md) for:
- Code style and formatting standards
- Testing requirements and procedures
- Pull request process and review criteria  
- Community guidelines and expectations

---

## 📄 License & Attribution

**Created by:** Kapil Dhanger  
**License:** MIT License  
**Repository:** [github.com/dhangerkapil/ai-foundry-e2e-lab](https://github.com/dhangerkapil/ai-foundry-e2e-lab)
