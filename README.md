# Azure-DALL-E-Image-Generation-App

This project is a simple Python-based application that integrates with Azure's OpenAI DALL-E API to generate AI-powered images from text prompts. The app leverages the Pillow library for image handling and requests for downloading the generated image.

# Features
- Generate AI-based images using Azure OpenAI DALL-E API.
- Save and display generated images locally.
- Customizable text prompts for generating creative images.
- Easily configurable API keys and endpoints using a .env file.

# Requirements
- Python 3.7 or higher.
- An active Azure OpenAI subscription and deployment for the DALL-E model.
The following Python libraries:
- openai
- Pillow
- requests
- dotenv

# Setup
Step 1: Clone the Repository
Clone the repository to your local machine:

bash
Copy code
git clone https://github.com/yourusername/azure-dalle-image-gen.git
cd azure-dalle-image-gen
Step 2: Create a Virtual Environment
To manage dependencies, create and activate a virtual environment:

bash
Copy code
# For Linux/macOS
python3 -m venv venv
source venv/bin/activate

# For Windows
python -m venv venv
.\venv\Scripts\activate
Step 3: Install Dependencies
Use pip to install the required libraries:

bash
Copy code
pip install -r requirements.txt
Step 4: Setup the .env File
To connect to Azure OpenAI, you’ll need to set your API keys and endpoints in a .env file. Create a .env file in the root directory with the following content:

bash
Copy code
# .env

# Azure OpenAI API Key
AZURE_OPENAI_API_KEY_DALL_E=your_azure_dalle_api_key

# Azure OpenAI Endpoint
AZURE_OPENAI_ENDPOINT_DALL_E=https://your-azure-openai-endpoint.com

# Azure OpenAI Deployment Name
AZURE_OPENAI_DEPLOYMENT_DALL_E=your_dalle_model_deployment_name
Replace your_azure_dalle_api_key, your_azure_openai_endpoint, and your_dalle_model_deployment_name with your actual values from the Azure portal.

Step 5: Run the Application
You can now run the image generation script by using the following command:

bash
Copy code
python app.py
This will generate an image based on the provided prompt, save it in the images/ directory, and display it.

# Folder Structure
bash
Copy code
azure-dalle-image-gen/
│
├── images/                # Contains generated images
│   └── generated-image.png
│
├── .env                   # Environment variables file (not included in repo)
├── app.py                 # Main Python script
├── README.md              # This file
├── requirements.txt       # Python dependencies
Prompt Customization
To modify the prompt for image generation, you can edit the prompt variable in the app.py script.

# Example:

python
Copy code
prompt = 'A futuristic city floating in the clouds, with glass towers shaped like giant trees, connected by glowing bridges...'
You can use your creativity to generate any kind of image you want using this prompt.

# Error Handling
The code includes error handling using try and finally blocks to ensure smooth operation. In case of issues such as invalid API keys, prompts, or requests, it will print the errors for easy debugging.

# Future Enhancements
Adding functionality to generate multiple images (n=1 can be updated).
Creating variations of the generated images.
Integrating a simple web interface using Streamlit for non-technical users.
License
This project is licensed under the MIT License - see the LICENSE file for details.

