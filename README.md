# Multi-Language-AI-Coding-assistant-using-Codellama

CodeGuru is an intelligent coding assistant powered by CodeLlama that helps developers with programming-related questions and tasks. It provides real-time code assistance, explanations, and guidance through a simple Gradio interface.

## Features

- Interactive chat interface for code-related queries
- Powered by CodeLlama language model
- Maintains conversation history for context
- Simple and intuitive Gradio UI
- Local deployment using Ollama

## Prerequisites

Before running CodeGuru, make sure you have the following installed:

- Python 3.8 or higher
- Ollama
- Required Python packages:
  - gradio
  - requests
  - json

## Installation

1. Pull and create the CodeGuru model:
```bash
# First pull CodeLlama
ollama pull codellama

# Then create CodeGuru model with the provided configuration
ollama create codeguru -f Modelfile
```

## Model Configuration

The CodeGuru model is built on top of CodeLlama with the following configuration in the Modelfile:

```
FROM codellama

# Set the temperature
PARAMETER temperature 1

# Set the system prompt
SYSTEM """
You are a code teaching assistant and a codeguru. Answer all the code related questions being asked.
"""
```

## Usage

1. Start the Ollama server:
```bash
ollama serve
```

2. Run the CodeGuru application:
```bash
python app.py
```

3. Open your web browser and navigate to the URL shown in the terminal (typically `http://localhost:7860`)

4. Enter your coding-related questions in the text box and receive responses from CodeGuru

## API Endpoints

The application communicates with Ollama's API endpoint:
- URL: `http://localhost:11434/api/generate`
- Method: POST
- Headers: `Content-Type: application/json`

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Built with [Ollama](https://ollama.ai)
- Powered by [CodeLlama](https://github.com/facebookresearch/codellama)
- UI created using [Gradio](https://gradio.app)

## Support

If you encounter any issues or have questions, please file an issue on the GitHub repository.
