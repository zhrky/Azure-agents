# Azure Agents

AZURE AGENTS is a web application that allows users to interact with various AI agents through a chat interface using tools. The application supports text and image inputs, and it can generate responses using Azure OpenAI services.  Generic copilot : genel sohbet akışı sağlayabilirsiniz. 
News copilot : Belli bir kategoride haberi, en son gelişmeleri öğrenebilirsiniz. Arkada Bing News search ve trending topics apileri çalışır.


**Project Aim**

## Features

- Chat with AI agents
- Supports text and image inputs
- Streaming responses
- Speech synthesis for responses
- WebRTC integration for video and audio


## Prerequisites

- [Azure subscription](https://azure.microsoft.com/en-gb/pricing/purchase-options/azure-account/search?icid=free-search&ef_id=_k_CjwKCAiAg8S7BhATEiwAO2-R6kCVtOWVtgADzLp3EZB9uLPuoyLOJKCSOugE7cw2Wx-UZVYssQRQBBoCGTUQAvD_BwE_k_&OCID=AIDcmmyckrgvvo_SEM__k_CjwKCAiAg8S7BhATEiwAO2-R6kCVtOWVtgADzLp3EZB9uLPuoyLOJKCSOugE7cw2Wx-UZVYssQRQBBoCGTUQAvD_BwE_k_&gad_source=1&gclid=CjwKCAiAg8S7BhATEiwAO2-R6kCVtOWVtgADzLp3EZB9uLPuoyLOJKCSOugE7cw2Wx-UZVYssQRQBBoCGTUQAvD_BwE)
- [Azure OpenAI](https://learn.microsoft.com/en-us/azure/ai-services/openai/)
- Python
    [Python 3.8+](https://www.python.org/downloads/)
    [Python VS Code extension](https://marketplace.visualstudio.com/items?itemName=ms-python.python)
    [Python Flask](https://pypi.org/project/Flask/)
    [Python - Flask-SocketIO](https://pypi.org/project/Flask-SocketIO/)
- [Azure Speech Service](https://azure.microsoft.com/en-us/products/ai-services/ai-speech)
- [Bing Search](https://www.microsoft.com/en-us/bing/apis/bing-news-search-api)


Azure Account - If you're new to Azure, get an Azure account for [free](https://azure.microsoft.com/en-us/free/?wt.mc_id=online-social-sicotin)
 and you'll get some free Azure credits to get started.
 
Azure subscription with access enabled for the Azure OpenAI Service - For more details, see the [Azure OpenAI Service documentation on how to get access](https://learn.microsoft.com/en-us/azure/ai-services/openai/overview#how-do-i-get-access-to-azure-openai).

Azure OpenAI resource - For these samples, you'll need to deploy models like GPT-3.5 Turbo, GPT 4, DALL-E, and Whisper. See the Azure OpenAI Service documentation for more details on [deploying models](https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/create-resource?pivots=web-portal) and [model availability](https://learn.microsoft.com/en-us/azure/ai-services/openai/concepts/models)
.
## Setup Instructions

1. **Clone the repository**:
    ```bash
    git clone <repository-url>
    cd <repository-directory>
    ```
    ```

1.1 **(Optional)create .venv**


2. **Install the required Python packages:**
    ```sh
    pip install -r requirements.txt
    ```

3. **Configure Azure OpenAI:**
    - Set up your Azure OpenAI service and obtain the API key and endpoint.
    - Update the `sampleconfig.py` file and rename it to `config.py` with your Azure OpenAI, Speech, Bing Search service credentials:
        ```python
        openai_key = 'your_openai_key'
        openai_endpoint = 'your_openai_endpoint'
        ...
      
        ```

4. **Run the application:**
    ```sh
    flask run
    ```

5. **Access the application:**
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

custom.html dosyası, kullanıcıların özel Copilot yapılandırmalarını oluşturup kullanmalarını sağlayan bir web sayfasıdır. Kullanıcılar, JSON formatında yapılandırma verileri girerek AI asistanlarının davranışını ve özelliklerini özelleştirebilirler. Bu yapılandırmalar bir form aracılığıyla sunucuya gönderilebilir. Kullanıcı dostu bir arayüz ve çeşitli stil öğeleriyle donatılan sayfa, özel AI asistanlarının hızlı ve kolay entegrasyonunu hedefler.
![custom page](https://github.com/user-attachments/assets/5ac4f312-13f2-4491-b1da-620ca6b9a114)



### Streaming Responses

- Responses will be displayed in streaming.
- You can listen to the responses using the speech synthesis feature, also you can change this via config file for example you can set the voice from this list according to available zone. And also you try on [speech coice gallery](https://speech.microsoft.com/portal/voicegallery)

### Example

1. **Text Input:**
    - Type your question in the input field and press Enter.
    - Example: "Merhaba son dakika haberleri nedir ?"

2. **Image Input:**
    - Click the paperclip icon to upload an image.
    - Example: Upload an image of a cat and ask, "Bu resimdeki kediyle ilgili haber var mıdır ?"

3. **Speech Input:**
    - Click the microphone icon and speak your question.
    - Example: "En son yayınlanan finans haberleri nedir ?"

4. **Additional Feature**
   - You can try azure open ai service with speech using speech.html file and command with :
       ```sh
     python app1.py
    ```
     
## Contributing

Contributions are welcome! Please fork the repository and submit a pull request for any improvements or bug fixes.

