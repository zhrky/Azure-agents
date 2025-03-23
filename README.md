# Azure Agents

**Azure AGENTS** is a web application that allows users to interact with various AI agents through a chat interface using tools. The application supports text and image inputs, and it can generate responses using Azure OpenAI services.  

### Project Aim

This project aims to provide a flexible interface for interacting with various AI agents, enabling text and image input, speech synthesis for responses, and WebRTC integration for video and audio.

## Features

- Chat with AI agents
- Supports text and image inputs
- Streaming responses
- Speech synthesis for responses
- WebRTC integration for video and audio

## Prerequisites

Before you start, ensure you have the following:

- **Azure subscription**: You can sign up for [Azure](https://azure.microsoft.com/en-gb/pricing/purchase-options/azure-account/search?icid=free-search&ef_id=_k_CjwKCAiAg8S7BhATEiwAO2-R6kCVtOWVtgADzLp3EZB9uLPuoyLOJKCSOugE7cw2Wx-UZVYssQRQBBoCGTUQAvD_BwE_k_&OCID=AIDcmmyckrgvvo_SEM__k_CjwKCAiAg8S7BhATEiwAO2-R6kCVtOWVtgADzLp3EZB9uLPuoyLOJKCSOugE7cw2Wx-UZVYssQRQBBoCGTUQAvD_BwE_k_&gad_source=1&gclid=CjwKCAiAg8S7BhATEiwAO2-R6kCVtOWVtgADzLp3EZB9uLPuoyLOJKCSOugE7cw2Wx-UZVYssQRQBBoCGTUQAvD_BwE)
- **Azure OpenAI Service**: Follow the [Azure OpenAI documentation](https://learn.microsoft.com/en-us/azure/ai-services/openai/) for setting up.
- **Python**: Ensure Python 3.8+ is installed. If not, download from [Python official site](https://www.python.org/downloads/).
- **Python Extensions**:
    - [Python VS Code extension](https://marketplace.visualstudio.com/items?itemName=ms-python.python)
    - [Flask](https://pypi.org/project/Flask/)
    - [Flask-SocketIO](https://pypi.org/project/Flask-SocketIO/)
- **Azure Speech Service**: You can use [Azure Speech Services](https://azure.microsoft.com/en-us/products/ai-services/ai-speech) for voice integration.
- **Bing Search API**: Integrate with [Bing News Search](https://www.microsoft.com/en-us/bing/apis/bing-news-search-api) for news-based agents.

## Setup Instructions

1. **Clone the repository**:
    ```bash
    git clone <repository-url>
    cd <repository-directory>
    ```

2. **(Optional) Create a Virtual Environment**:
    You can create a virtual environment for better dependency management:
    ```bash
    python -m venv .venv
    source .venv/bin/activate  # On Windows: .venv\Scripts\activate
    ```

3. **Install the required Python packages**:
    ```bash
    pip install -r requirements.txt
    ```

4. **Configure Azure OpenAI**:
    - Set up your Azure OpenAI service and obtain the API key and endpoint.
    - Update the `sampleconfig.py` file and rename it to `config.py` with your credentials for Azure OpenAI, Speech, and Bing Search:
      ```python
      openai_key = 'your_openai_key'
      openai_endpoint = 'your_openai_endpoint'
      ...
      ```

5. **Run the application**:
    ```bash
    flask run
    ```

6. **Access the application**:
    - Open your web browser and navigate to `http://localhost:5000`.

## Usage

### Selecting an AI Agent

- Navigate to the hub to select an AI agent.
- Each agent has a unique set of capabilities and initial prompts.
- ![intro page](https://github.com/user-attachments/assets/54543921-42b0-41f7-b205-be552462d77b)

### Starting a Chat Session

- Click on an agent to start a chat session.
- Use the input field to type your questions or upload images.
- Click the microphone icon to use speech input.
- ![news page](https://github.com/user-attachments/assets/0cfedda3-b771-4efd-a201-938a659e496b)

### Customize Your Chat Session

The **custom.html** file allows users to create and use custom configurations for Copilot. Users can input configuration data in JSON format to modify the behavior and features of AI assistants. This configuration is submitted to the server via a form. The page features a user-friendly interface and various style elements to facilitate easy integration of custom AI assistants.
![custom page](https://github.com/user-attachments/assets/5ac4f312-13f2-4491-b1da-620ca6b9a114)

### Streaming Responses

- Responses will be displayed in real-time as they are generated.
- Speech synthesis can be enabled for listening to responses.
- You can change the voice settings from the config file and adjust them based on available zones. Try out the [speech voice gallery](https://speech.microsoft.com/portal/voicegallery).

### Example

1. **Text Input:**
    - Type your question and press Enter.
    - Example: "Merhaba son dakika haberleri nedir ?"

2. **Image Input:**
    - Click the paperclip icon to upload an image.
    - Example: Upload an image of a cat and ask, "Bu resimdeki kediyle ilgili haber var mıdır ?"

3. **Speech Input:**
    - Click the microphone icon and speak your question.
    - Example: "En son yayınlanan finans haberleri nedir ?"

4. **Additional Feature:**
    - You can try Azure OpenAI services with speech by running the following command:
    ```bash
    python app1.py
    ```

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request for any improvements or bug fixes.

---

**Note**: For more details on Azure OpenAI, see the [Azure OpenAI documentation](https://learn.microsoft.com/en-us/azure/ai-services/openai/overview#how-do-i-get-access-to-azure-openai).
