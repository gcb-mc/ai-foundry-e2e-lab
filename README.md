# 🚀 Azure AI Foundry E2E Laboratory

<di## 🔧 Environment Setup

### 📋 System Requirementslign="center">

[![Azure AI Foundry](https://img.shields.io/badge/Azure%20AI-Foundry-blue?style=for-the-badge&l## 📚 Learning Modules

Our laboratory follows a progressive learning architecture, designed to build expertise systematically:icrosoft)](https://ai.azure.com)
[![Python](https://img.shields.io/badge/Python-3.10+-green?style=for-the-badge&logo=python)](https://python.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-Lab-orange?style=for-the-badge&logo=jupyter)](https://jupyter.org)

**End-to-End AI Development Laboratory by Kapil Dhanger**

*Master Azure AI Foundry through hands-on experimentation and real-world applications*

---

🎯 [Getting Started](#-getting-started) • 📚 [Learning Modules](#-learning-modules) • 🔧 [Setup Guide](#-environment-setup) • 🤖 [Multi-Agent Systems](#-multi-agent-systems) • 📊 [Project Gallery](#-project-gallery)

</div>

---

## 🎯 Mission Statement

This comprehensive laboratory transforms you from an AI enthusiast into an Azure AI Foundry expert. Through progressive, hands-on modules, you'll master:

🔬 **Core AI Engineering**
- Advanced model deployment strategies and optimization techniques
- Production-ready authentication and security implementation  
- Scalable project architecture and configuration management

🤖 **Intelligent Agent Development**
- Multi-modal AI agents with specialized health and wellness expertise
- Advanced RAG (Retrieval-Augmented Generation) implementations
- Real-time decision-making systems and automated workflows

🏗️ **Enterprise-Grade Solutions**
- End-to-end AI application development with modern frameworks
- Multi-agent orchestration and coordination patterns
- Quality assurance through comprehensive evaluation and monitoring

> **🎓 Laboratory Format**: 4-5 hour intensive hands-on experience  
> **🎯 Target Audience**: Developers, AI practitioners, and solution architects  
> **💡 Learning Approach**: Progressive complexity with real-world applications

## � Environment Setup## 🔧 Environment Setup

### 📋 System Requirements

**Essential Components:**
- 🐍 [Python 3.10+](https://www.python.org/downloads/) - Latest stable version recommended
- ☁️ [Azure Subscription](https://ai.azure.com) - Active subscription with Azure AI Foundry access
- 💻 Development Environment: Choose your preferred option
  - [Visual Studio Code](https://code.visualstudio.com/) with Python & Jupyter extensions
  - [GitHub Codespaces](https://github.com/features/codespaces) for cloud development
  - [JupyterLab](https://jupyter.org/install) for notebook-first development
- 🛠️ [Azure CLI](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli) - For Azure resource management
- 📦 [Git](https://git-scm.com/downloads) - Version control and repository management

**Knowledge Prerequisites:**
- ✅ Intermediate Python programming skills
- ✅ Basic understanding of machine learning concepts
- ✅ Familiarity with REST APIs and web services
- ✅ Experience with Azure services (recommended)

---

## 🚀 Getting Started

### Step 1: Repository Setup

```bash
# Clone the laboratory repository
git clone https://github.com/dhangerkapil/ai-foundry-e2e-lab.git
cd ai-foundry-e2e-lab

# Verify Python version
python --version  # Should be 3.10 or higher
```

### Step 2: Python Environment Configuration

**Option A: Using UV (Recommended - Fastest)**
```bash
# Install UV package manager
# Unix/Linux/macOS
curl -LsSf https://astral.sh/uv/install.sh | sh

# Windows PowerShell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"

# Create and activate virtual environment
uv venv
source .venv/bin/activate     # Unix/Linux/macOS
# OR
.\.venv\Scripts\Activate.ps1  # Windows PowerShell
```

**Option B: Using Standard venv**
```bash
# Create virtual environment
python -m venv .venv

# Activate environment
source .venv/bin/activate     # Unix/Linux/macOS
# OR  
.\.venv\Scripts\activate      # Windows
```

### Step 3: Azure AI Foundry Platform Setup

#### 🏗️ Infrastructure Deployment

**3a. Create Azure AI Foundry Project**
1. Navigate to [Azure AI Foundry Portal](https://ai.azure.com)
2. Select **"Create new project"** → Follow the AI Foundry Wizard
3. Configure your project with these specifications:
   - **Region**: Choose based on model availability (East US, West Europe recommended)
   - **Pricing Tier**: Standard (required for advanced features)
   - **Resource Group**: Create new or use existing

**3b. Model Deployment Strategy**
Deploy these essential models with **maximum TPM settings**:

| Model Type | Recommended Models | Purpose | Configuration |
|------------|-------------------|---------|---------------|
| **Chat/Completion** | `gpt-4o`, `gpt-4o-mini` | Primary reasoning & conversation | Max TPM, DataZone-Standard |
| **Embeddings** | `text-embedding-3-large` | Vector search & RAG | Standard deployment |
| **Specialized** | `phi-4`, `deepseek-r1` | Domain-specific tasks | Global-Standard |

**3c. Connection Configuration**
Essential integrations to configure:
- 🔍 [Bing Search Grounding](https://learn.microsoft.com/en-us/azure/ai-services/agents/how-to/tools/bing-grounding) - Real-time web data access
- 🔎 [Azure AI Search](https://learn.microsoft.com/en-us/azure/search/search-what-is-azure-search) - Document indexing and retrieval
- 🔐 **Access Control**: Add your account to `Azure AI Developer` role

### Step 4: Environment Configuration

#### 📝 Configuration File Setup
```bash
# Create your environment configuration
cp .env.example .env
```

#### 🔧 Critical Environment Variables

**Core Project Settings:**
```env
# Azure AI Foundry Project Connection
PROJECT_CONNECTION_STRING=your-project-connection-string-from-azure-ml-workspace
MODEL_DEPLOYMENT_NAME=your-primary-model-deployment-name
EMBEDDING_MODEL_DEPLOYMENT_NAME=your-embedding-model-deployment-name

# Azure Authentication
TENANT_ID=your-azure-tenant-id-from-portal

# Advanced Features  
BING_CONNECTION_NAME=your-bing-search-connection-name
SERVERLESS_MODEL_NAME=your-serverless-model-deployment-name

# Monitoring & Telemetry
AZURE_TRACING_GEN_AI_CONTENT_RECORDING_ENABLED=true
AZURE_SDK_TRACING_IMPLEMENTATION=opentelemetry
```

> ⚠️ **Important**: Ensure your `MODEL_DEPLOYMENT_NAME` supports [Azure AI Agents Service](https://learn.microsoft.com/en-us/azure/ai-services/agents/concepts/model-region-support). For Bing integration, use `gpt-4o-mini`.

### Step 5: Dependency Installation

#### 🚀 Fast Track Installation (Recommended)
```bash
# Install all dependencies at once
uv pip install azure-identity azure-ai-projects azure-ai-inference[opentelemetry] \
               azure-search-documents azure-ai-evaluation azure-monitor-opentelemetry \
               ipykernel jupyterlab notebook pandas numpy matplotlib seaborn

# Register Jupyter kernel
python -m ipykernel install --user --name=ai-foundry-lab --display-name="AI Foundry Lab"

# Optional: Full feature set (includes documentation tools)
uv pip install -r requirements.txt
```

#### 🔧 Development Environment Selection

**Option A: Visual Studio Code (Recommended)**
```bash
# Install VS Code extensions (run these in VS Code terminal)
code --install-extension ms-python.python
code --install-extension ms-toolsai.jupyter
```
- Open any `.ipynb` file
- Select kernel: `AI Foundry Lab` from the kernel picker

**Option B: JupyterLab (Data Science Focused)**
```bash
# Launch JupyterLab
jupyter lab
# Navigate to notebooks and select the AI Foundry Lab kernel
```

**Option C: GitHub Codespaces (Cloud Development)**
- Click **"Code"** → **"Create codespace"** on GitHub
- Wait for automatic environment setup
- All dependencies pre-installed and ready

---

## � Learning Modules

## 📚 Learning Modules

Our laboratory follows a progressive learning architecture, designed to build expertise systematically:

### 🎯 Module 1: Foundation & Authentication
**Location:** `1-introduction/`

| Notebook | Focus Area | Key Skills |
|----------|------------|------------|
| 🔐 [Authentication](1-introduction/1-authentication.ipynb) | Azure credential management & security | DefaultAzureCredential, token lifecycle, role-based access |
| ⚙️ [Environment Setup](1-introduction/2-environment_setup.ipynb) | Development environment optimization | Project configuration, SDK integration, debugging |
| 🚀 [Quick Start](1-introduction/3-quick_start.ipynb) | Core Azure AI Foundry operations | Model deployment, basic inference, connection testing |

### 🤖 Module 2: Advanced AI Engineering
**Location:** `2-notebooks/`

#### 💬 Chat Completion & RAG Systems
**Path:** `1-chat_completion/`
- **Basic Chat Completion**: Foundation models and prompt engineering
- **Embeddings & Vector Search**: Semantic understanding and similarity
- **Retrieval-Augmented Generation**: Context-aware AI responses
- **Phi-4 Integration**: Microsoft's specialized reasoning model
- **DeepSeek R1**: Advanced reasoning and code generation

#### 🤖 Intelligent Agent Development
**Path:** `2-agent_service/`
- **Agent Fundamentals**: Architecture patterns and lifecycle management
- **Code Interpreter**: Automated code execution and analysis
- **File Search**: Document processing and knowledge extraction
- **Bing Grounding**: Real-time web data integration
- **Azure AI Search**: Enterprise search and retrieval
- **Azure Functions**: Serverless agent deployment

#### 🔄 Multi-Agent Orchestration
**Path:** `multi-agent/`
- **Multi-Agent Solutions**: Collaborative AI system design
- **Distributed Tracing**: End-to-end monitoring and debugging
- **Agent Coordination**: Communication protocols and task distribution

#### 🏗️ Advanced Frameworks
**Path:** `4-frameworks/`
- **RAG + Semantic Kernel**: Microsoft's orchestration framework
- **AutoGen Multi-Agent RAG**: Automated agent generation and management
- **Health Analytics**: Specialized domain applications with personalized insights

#### 📊 Quality & Operations
**Path:** `3-quality_attributes/`
- **Observability**: Comprehensive monitoring and telemetry
- **Evaluation Systems**: Automated quality assessment and benchmarking
- **Production Readiness**: Deployment strategies and scaling patterns

---

## 🤖 Multi-Agent Systems

Explore cutting-edge multi-agent architectures that power enterprise AI solutions:

### 🔄 Collaborative Intelligence
- **Agent Specialization**: Domain-specific expertise and role assignment
- **Task Orchestration**: Complex workflow automation and management  
- **Knowledge Sharing**: Inter-agent communication and data exchange
- **Failure Recovery**: Resilient system design and error handling

### 📊 Advanced Monitoring
- **Distributed Tracing**: End-to-end request tracking across agent networks
- **Performance Analytics**: Real-time metrics and optimization insights
- **Quality Assurance**: Automated testing and validation frameworks

---

## 📊 Project Gallery

### 🏥 End-to-End Health AI Platform
**Location:** `3-ai-native-e2e-sample/`

A production-ready application demonstrating enterprise AI patterns:

#### 🎯 Architecture Highlights
- **Backend**: FastAPI with Azure AI SDK integration
- **Frontend**: Modern React with real-time updates  
- **AI Agents**: Specialized health and wellness advisors
- **Data Integration**: Multiple data sources and formats
- **Monitoring**: Comprehensive observability and analytics

#### 🔧 Technical Features
- **Microservices Architecture**: Scalable and maintainable design
- **Event-Driven Processing**: Asynchronous workflow management
- **API-First Design**: RESTful interfaces with OpenAPI documentation
- **Security**: Enterprise-grade authentication and authorization

---

## 🛠️ Troubleshooting & Support

### ⚡ Quick Fixes

**Kernel Issues in VS Code:**
```bash
# Refresh kernel registration
python -m ipykernel install --user --name=ai-foundry-lab --display-name="AI Foundry Lab"
# Reload VS Code window: Ctrl+Shift+P → "Developer: Reload Window"
```

**Environment Activation Problems:**
```bash
# Windows PowerShell execution policy
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser

# Verify virtual environment
python -c "import sys; print(sys.executable)"
```

**Azure Authentication Issues:**
```bash
# Clear cached credentials
az account clear
az login --tenant YOUR_TENANT_ID

# Verify access
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

---

<div align="center">

**🚀 Ready to become an Azure AI Foundry expert?**

[Start Your Journey](1-introduction/1-authentication.ipynb) • [Join Our Community](https://github.com/dhangerkapil/ai-foundry-e2e-lab/discussions) • [Report Issues](https://github.com/dhangerkapil/ai-foundry-e2e-lab/issues)

*Built with ❤️ by Kapil Dhanger*

</div>




