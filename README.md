# LLM Model Response Diff Tool 🔍

A modern web application for comparing responses from different Large Language Models (LLMs) side-by-side. Compare OpenAI GPT models with Google Gemini or Anthropic, analyze performance metrics, and visualize differences with highlighting.

![image](https://github.com/user-attachments/assets/7fbaf992-6410-47f3-9371-6ac0e161dccf)
![image](https://github.com/user-attachments/assets/4f64ae7f-f9e4-4ce0-baa2-0d594f2020c3)

## ✨ Features

- **🔀 Side-by-Side Comparison**: Compare responses from any two LLM models
- **⚡ Real-Time Metrics**: Track response time, token usage, and performance
- **🎨 Intelligent Highlighting**: Visual diff highlighting to spot differences at a glance
- **🌐 Multi-Provider Support**: Works with OpenAI, Google Gemini and Anthropic
- **📱 Responsive Design**: Beautiful, modern UI that works on desktop and mobile
- **🔒 Secure**: API keys are never stored or transmitted to external servers
- **⚙️ Configurable**: Flexible endpoint and model configuration

## 🚀 Quick Start

### Option 1: Use Online (Recommended)
Simply open the `llm-diff-tool.html` file in your web browser - no installation required!

### Option 2: Local Development
```bash
# Clone the repository
git clone https://github.com/yourusername/llm-diff-tool.git
cd llm-diff-tool

# Open in your browser
open llm-diff-tool.html
# or
python -m http.server 8000  # Then visit http://localhost:8000
```

## 📖 Usage

1. **Configure Your Models**
   - Enter API endpoints for both models
   - Add your API keys (stored locally only)
   - Specify model names (e.g., `gpt-5-nano`, `gemini-2.5-flash`, `claude-3-sonnet-20240229`)

2. **Enter Your Prompt**
   - Type or paste the prompt you want both models to respond to

3. **Compare**
   - Click "Compare Responses" to get results from both models
   - View side-by-side responses with difference highlighting
   - Analyze performance metrics and token usage

4. **Toggle Features**
   - Enable/disable difference highlighting as needed
   - Scroll through longer responses easily

## 🔧 Supported Providers

### OpenAI
```
Endpoint: https://api.openai.com/v1/responses
Models: gpt-4, gpt-4-turbo, gpt-3.5-turbo, etc.
```

### Google Gemini
```
Endpoint: https://generativelanguage.googleapis.com/v1beta/models
Models: gemini-2.5-flash, gemini-2.5-pro, etc.
```

### Anthropic
```
Endpoint: https://api.anthropic.com/v1/messages
Models: claude-3-opus-20240229, claude-3-sonnet-20240229, etc.
```

### Local APIs
Any API that follows the OpenAI chat completions format:
```
Endpoint: http://localhost:8000/v1/chat/completions
Models: llama-2-7b, mistral-7b, etc.
```

## ⚙️ Configuration

### API Key Setup
1. **OpenAI**: Get your API key from [OpenAI Platform](https://platform.openai.com/api-keys)
2. **Google Gemini**: Get your API key from [Google Gemini AI Studio](https://aistudio.google.com/)
3. **Anthropic**: Get your API key from [Anthropic Console](https://console.anthropic.com/)
4. **Local Models**: Configure according to your local setup

### Request Parameters
The tool sends requests with these default parameters:
- `max_output_tokens`: 1000
- Message format: OpenAI chat completions style

## 📊 Metrics Tracked

- **Response Time**: How long each model took to respond
- **Prompt Tokens**: Number of tokens in your input (Not for Google Gemini)
- **Completion Tokens**: Number of tokens in the model's response (Not for Google Gemini)
- **Total Tokens**: Combined token usage (Not for Google Gemini)
- **Model Names**: For easy identification

## 🎨 Features in Detail

### Difference Highlighting
The tool uses intelligent word-level comparison to highlight:
- **🔴 Removed content**: Text present in Model 1 but not Model 2
- **🟢 Added content**: Text present in Model 2 but not Model 1
- **⚪ Unchanged content**: Text that's identical in both responses

### Performance Comparison
Track and compare:
- Response latency
- Token efficiency
- Output length
- Model behavior differences

## 🛡️ Security & Privacy

- **No Data Storage**: All comparisons happen locally in your browser
- **No External Requests**: API keys and responses never leave your device
- **Direct API Calls**: Connects directly to LLM providers, no intermediary servers

## 🐛 Troubleshooting

### Common Issues

**API Key Errors**
- Ensure your API keys are valid and have sufficient credits
- Check that you're using the correct endpoint for each provider

**CORS Errors**
- Some browsers may block direct API calls
- Use a local server (like `python -m http.server`) if needed

**Response Format Issues**
- Verify your model names are correct
- Ensure the API endpoint supports the chat completions format

**Slow Performance**
- Check your internet connection
- Some models may have longer response times

## 📝 Changelog

### v1.0.1
- Google Gemini support
- OpenAI change from Completions API to Responses API

### v1.0.0
- Initial release
- OpenAI and Anthropic support
- Real-time difference highlighting
- Performance metrics tracking
- Responsive design

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
