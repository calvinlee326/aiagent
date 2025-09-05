# AI Agent Workflow Patterns

A comprehensive collection of AI agent implementations using OpenAI's GPT models, featuring structured outputs, tool calling, and various workflow patterns.

## 🚀 Features

- **Structured Outputs**: Use Pydantic models for type-safe AI responses
- **Tool Integration**: Weather APIs and external service integration
- **Workflow Patterns**: 
  - Prompt Chaining with gate checks
  - Parallel processing
  - Request routing
- **Interactive Examples**: Jupyter notebooks with detailed demonstrations
- **Knowledge Retrieval**: Document-based Q&A system

## 📁 Project Structure

```
aiagent/
├── basic/                    # Core AI agent examples
│   ├── basic.py             # Simple completion example
│   ├── structure.py         # Structured output parsing
│   ├── tools.py             # Function calling with tools
│   ├── retrieval.py         # RAG (Retrieval-Augmented Generation)
│   └── kb.json              # Knowledge base sample data
├── workflow-pattern/         # Advanced workflow implementations
│   ├── prompt-chaining.py   # Sequential LLM calls with validation
│   ├── parallization.py     # Concurrent processing patterns
│   └── routing.py           # Request classification and routing
├── agent_demo.ipynb         # Interactive Jupyter demonstration
├── requirements.txt         # Python dependencies
└── README.md               # This file
```

## 🛠️ Installation

### Prerequisites
- Python 3.11+
- OpenAI API key

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/calvinlee326/aiagent.git
   cd aiagent
   ```

2. **Create virtual environment**
   ```bash
   python -m venv .venv
   source .venv/bin/activate  # On Windows: .venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure environment**
   ```bash
   # Create .env file
   echo "OPENAI_API_KEY=your_openai_api_key_here" > .env
   ```

## 🎯 Usage Examples

### Basic Structured Output
```python
from basic.structure import CalendarEvent
# Extracts structured event data from natural language
```

### Tool Integration
```python
from basic.tools import get_weather
# Calls external APIs with AI-generated parameters
```

### Prompt Chaining Workflow
```python
from workflow_pattern.prompt_chaining import process_calendar_request

# Multi-step validation and processing
result = process_calendar_request("Schedule a meeting next Tuesday at 2pm")
```

### Interactive Exploration
```bash
# Launch Jupyter for hands-on examples
jupyter lab agent_demo.ipynb
```

## 🔧 Configuration

### Environment Variables
- `OPENAI_API_KEY`: Your OpenAI API key (required)

### Model Configuration
- Default model: `gpt-4o` (supports structured outputs)
- Fallback model: `gpt-4.1-mini` for basic operations

## 📊 Workflow Patterns

### 1. Prompt Chaining (`prompt-chaining.py`)
Sequential LLM calls with validation gates:
- **Step 1**: Event extraction and confidence scoring
- **Step 2**: Detailed parsing (if confidence > 0.7)
- **Step 3**: Confirmation message generation

### 2. Parallelization (`parallization.py`)
Concurrent processing for efficiency:
- Multiple AI calls in parallel
- Result aggregation and synthesis
- Error handling and fallbacks

### 3. Routing (`routing.py`)
Smart request classification:
- Intent detection
- Route to appropriate handlers
- Conditional workflow execution

## 🧪 Testing

Run individual examples:
```bash
# Basic examples
python basic/structure.py
python basic/tools.py

# Workflow patterns
python workflow-pattern/prompt-chaining.py
python workflow-pattern/parallization.py
```

## 📚 Dependencies

Key packages:
- `openai>=1.100.0` - OpenAI API client
- `pydantic>=2.0.0` - Data validation and parsing
- `python-dotenv` - Environment variable management
- `requests` - HTTP client for external APIs
- `jupyterlab` - Interactive development environment

See `requirements.txt` for complete dependency list.

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Commit changes: `git commit -m "Add feature"`
4. Push to branch: `git push origin feature-name`
5. Submit a pull request

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🔗 Resources

- [OpenAI API Documentation](https://platform.openai.com/docs)
- [Pydantic Documentation](https://docs.pydantic.dev/)
- [Structured Outputs Guide](https://platform.openai.com/docs/guides/structured-outputs)

---

**Built with ❤️ using OpenAI GPT-4 and modern Python practices**
