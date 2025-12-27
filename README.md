# 🤖 AI-DotNet Integration

**AI Service Integration Examples for .NET Developers - OpenAI, Azure AI, ML.NET, and More**

[![.NET](https://img.shields.io/badge/.NET-8.0-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)](https://dotnet.microsoft.com/)
[![C#](https://img.shields.io/badge/C%23-12.0-239120?style=for-the-badge&logo=csharp&logoColor=white)](https://docs.microsoft.com/en-us/dotnet/csharp/)
[![OpenAI](https://img.shields.io/badge/OpenAI-API-412991?style=for-the-badge&logo=openai&logoColor=white)](https://platform.openai.com/)
[![Azure AI](https://img.shields.io/badge/Azure-AI-0078D4?style=for-the-badge&logo=microsoft-azure&logoColor=white)](https://azure.microsoft.com/en-us/solutions/ai/)
[![ML.NET](https://img.shields.io/badge/ML.NET-3.0-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)](https://dotnet.microsoft.com/apps/machinelearning-ai/ml-dotnet)
[![License](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](LICENSE)

> A comprehensive collection of **production-ready** AI integration examples for .NET 8 developers. Build intelligent applications with OpenAI, Azure AI, ML.NET, and Semantic Kernel.

---

## 🌟 Features

✅ **OpenAI Integration** - GPT-4, DALL-E, Embeddings, Whisper, Function Calling  
✅ **Azure AI Services** - Azure OpenAI, Cognitive Services, AI Search, Form Recognizer  
✅ **ML.NET Examples** - Classification, Regression, Recommendations, Anomaly Detection  
✅ **Semantic Kernel** - Plugins, Planners, Memory, RAG Implementations  
✅ **Advanced Scenarios** - RAG Chatbots, Document Analysis, Multi-Modal Apps  
✅ **Production Ready** - Error Handling, Rate Limiting, Caching, Monitoring  

---

## 🚀 Quick Start

### **Prerequisites:**
- [.NET 8 SDK](https://dotnet.microsoft.com/download/dotnet/8.0)
- OpenAI API Key ([Get one here](https://platform.openai.com/api-keys))
- Azure Subscription (optional, for Azure AI examples)

### **Clone & Run:**

```bash
# Clone the repository
git clone https://github.com/carbonfin7/AI-DotNet-Integration.git
cd AI-DotNet-Integration

# Set up your API keys
cp appsettings.example.json appsettings.json
# Edit appsettings.json with your API keys

# Run an example (e.g., OpenAI Chat)
cd src/01-OpenAI-Examples/ChatCompletion
dotnet run

# Or use Docker
docker-compose up
```

---

## 📂 Project Structure

```
AI-DotNet-Integration/
│
├── 📁 01-OpenAI-Examples/          # OpenAI API integration
│   ├── ChatCompletion/             # GPT-4/3.5 chat examples
│   ├── ImageGeneration/            # DALL-E 3 integration
│   ├── Embeddings/                 # Text embeddings & similarity
│   ├── TextToSpeech/               # Whisper TTS integration
│   └── FunctionCalling/            # OpenAI function calling
│
├── 📁 02-Azure-AI-Examples/        # Azure AI Services
│   ├── AzureOpenAI/                # Azure OpenAI service
│   ├── CognitiveServices/          # Vision, Speech, Language
│   ├── AzureML/                    # Azure Machine Learning
│   └── AISearch/                   # Azure AI Search (RAG)
│
├── 📁 03-MLNet-Examples/           # ML.NET machine learning
│   ├── SentimentAnalysis/          # Text classification
│   ├── ImageClassification/        # Image recognition
│   ├── Regression/                 # Price prediction
│   ├── Recommendation/             # Recommendation engine
│   └── AnomalyDetection/           # Outlier detection
│
├── 📁 04-SemanticKernel-Examples/  # Semantic Kernel AI orchestration
│   ├── BasicSetup/                 # SK fundamentals
│   ├── Plugins/                    # Custom SK plugins
│   ├── Planners/                   # Multi-step AI tasks
│   ├── Memory/                     # Semantic memory
│   └── RAG-Pipeline/               # Retrieval Augmented Generation
│
├── 📁 05-Advanced-Scenarios/       # Real-world applications
│   ├── ChatbotWithRAG/             # Full chatbot with vector DB
│   ├── DocumentAnalysis/           # PDF/Document processing
│   ├── MultiModalApp/              # Text + Image + Audio
│   ├── AgentOrchestration/         # Multi-agent systems
│   └── RealTimeStreaming/          # Streaming responses
│
└── 📁 06-Production-Ready/         # Production best practices
    ├── RateLimiting/               # API rate limit handling
    ├── ErrorHandling/              # Resilience patterns
    ├── Caching/                    # Redis caching strategies
    ├── Monitoring/                 # Application Insights
    └── CostOptimization/           # Token usage optimization
```

---

## 🛠️ Tech Stack

### **Core Technologies:**
| Technology | Purpose | Version |
|------------|---------|---------|
| **.NET** | Runtime & Framework | 8.0 |
| **C#** | Programming Language | 12 |
| **OpenAI API** | GPT, DALL-E, Whisper | Latest |
| **Azure AI** | Azure OpenAI, Cognitive Services | Latest |
| **ML.NET** | Machine Learning | 3.0+ |
| **Semantic Kernel** | AI Orchestration | Latest |

### **Key Libraries:**
- `Azure.AI.OpenAI` - Azure OpenAI SDK
- `Betalgo.OpenAI` - OpenAI SDK for .NET
- `Microsoft.SemanticKernel` - AI orchestration framework
- `Microsoft.ML` - ML.NET framework
- `Polly` - Resilience & retry policies
- `Redis.OM` - Redis caching & vector search
- `Pinecone.NET` - Vector database client

---

## 💡 Example: OpenAI Chat Completion

```csharp
using Azure.AI.OpenAI;
using OpenAI.Chat;

// Initialize client
var client = new OpenAIClient("YOUR_API_KEY");
var chatClient = client.GetChatClient("gpt-4");

// Create chat completion
var messages = new List<ChatMessage>
{
    new SystemChatMessage("You are a helpful .NET programming assistant."),
    new UserChatMessage("Explain dependency injection in .NET 8")
};

var response = await chatClient.CompleteChatAsync(messages);

Console.WriteLine(response.Value.Content[0].Text);
```

### **Output:**
```
Dependency Injection (DI) in .NET 8 is a design pattern that helps you create loosely coupled applications...
```

**[See full example →](src/01-OpenAI-Examples/ChatCompletion)**

---

## 🎯 Use Cases

| Use Case | Example | Technologies |
|----------|---------|--------------|
| **AI Chatbot** | Customer support bot with RAG | OpenAI + Pinecone + Redis |
| **Document Analysis** | Extract data from PDFs/invoices | Azure Form Recognizer + GPT-4 |
| **Image Generation** | Create marketing images | DALL-E 3 + Azure Blob Storage |
| **Sentiment Analysis** | Analyze customer reviews | ML.NET + Azure Cognitive Services |
| **Code Assistant** | AI-powered code suggestions | GPT-4 + Semantic Kernel |
| **Voice Assistant** | Speech-to-text + AI responses | Whisper + GPT-4 + TTS |

---

## 🔑 Configuration

### **1. Create `appsettings.json`:**

```json
{
  "OpenAI": {
    "ApiKey": "sk-proj-...",
    "Organization": "org-..."
  },
  "AzureOpenAI": {
    "Endpoint": "https://YOUR-RESOURCE.openai.azure.com/",
    "ApiKey": "YOUR_AZURE_API_KEY",
    "DeploymentName": "gpt-4"
  },
  "AzureAI": {
    "ComputerVision": {
      "Endpoint": "https://YOUR-RESOURCE.cognitiveservices.azure.com/",
      "ApiKey": "YOUR_VISION_API_KEY"
    }
  },
  "Pinecone": {
    "ApiKey": "YOUR_PINECONE_API_KEY",
    "Environment": "us-east-1-aws"
  },
  "Redis": {
    "ConnectionString": "localhost:6379"
  }
}
```

### **2. Or use Environment Variables:**

```bash
# Windows (PowerShell)
$env:OPENAI_API_KEY="sk-proj-..."
$env:AZURE_OPENAI_ENDPOINT="https://..."
$env:AZURE_OPENAI_API_KEY="..."

# Linux/Mac
export OPENAI_API_KEY="sk-proj-..."
export AZURE_OPENAI_ENDPOINT="https://..."
export AZURE_OPENAI_API_KEY="..."
```

---

## 📖 Documentation

| Document | Description |
|----------|-------------|
| [Getting Started](docs/GettingStarted.md) | Comprehensive setup guide |
| [Best Practices](docs/BestPractices.md) | AI integration best practices |
| [Prompt Engineering](docs/PromptEngineering.md) | Effective prompt design |
| [Cost Analysis](docs/CostAnalysis.md) | Token usage & pricing optimization |
| [Troubleshooting](docs/Troubleshooting.md) | Common issues & solutions |

---

## 🧪 Testing

```bash
# Run all tests
dotnet test

# Run specific test project
cd tests/UnitTests
dotnet test

# Run with coverage
dotnet test /p:CollectCoverage=true
```

---

## 🐳 Docker Support

```bash
# Build and run with Docker Compose
docker-compose up

# Build specific service
docker build -t ai-dotnet-chatbot -f docker/Dockerfile .

# Run container
docker run -p 5000:5000 ai-dotnet-chatbot
```

---

## 🤝 Contributing

Contributions are welcome! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for details.

### **Ways to Contribute:**
- 🐛 Report bugs
- 💡 Suggest new features
- 📝 Improve documentation
- 🔧 Submit pull requests
- ⭐ Star the repository

---

## 🌟 Show Your Support

If this project helped you, please consider:
- ⭐ **Starring** the repository
- 🍴 **Forking** for your own projects
- 📢 **Sharing** with other .NET developers
- 💬 **Providing feedback** via issues
