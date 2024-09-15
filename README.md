# Smart-Content-Creator

This project is an automated content generation tool that creates blog posts based on user-provided topics. It leverages Hugging Face's GPT-2 model integrated with TensorFlow for text generation and uses Flask for the web interface. The application also employs LangChain to manage interactions with the language model, making it customizable and user-friendly.

## Features
- Generate Blog Content: Creates blog posts based on topics entered by the user.
- Hugging Face GPT-2 Integration: Utilizes GPT-2 with TensorFlow for generating human-like text.
- Web Interface: Simple and interactive web interface built with Flask for easy topic input and content generation.
- Customizable Parameters: Adjust generation parameters like temperature to control the creativity of the generated text.

## Requirements
- Python 3.8+
- Flask
- TensorFlow
- Transformers (Hugging Face)
- LangChain

  
## Installation
Follow these steps to set up and run the application locally:

1. Clone the Repository:
```bash
git clone https://github.com/rajatbutola/Smart-Content-Creator.git
cd content-generator-tool
```
2. Create and Activate a Virtual Environment:

```bash
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
```
3. Install Required Packages:
 ```bash
pip install -r requirements.txt

```
## Usage
Start the Flask Server:

```bash
python app.py
```
## Access the Web Interface:

Open your web browser and go to http://127.0.0.1:5000.

## Generate Blog Content:

- Enter the topic you wish to generate content for.
- Click the Generate button to receive an AI-generated blog post.

## Configuration
You can modify the text generation parameters such as temperature directly in the code. This controls the creativity and randomness of the generated content.

```bash
# Define a prompt template
prompt = f"Generate a detailed blog post on the topic: {topic}"

# Generate text with the Hugging Face model
generated_text = model.generate(
    input_ids=tokenizer.encode(prompt, return_tensors='tf'),
    max_length=500,
    num_return_sequences=1,
    temperature=0.7  # Adjust temperature here
)
```
```temperature```: Lower values (closer to 0) make the model more conservative and deterministic, while higher values introduce more creativity and randomness into the output.








