## VisionText RAG QA Chatbot

### Overview
The **QA RAG Chatbot** is a Streamlit-based application designed to analyze uploaded images and answer user queries about the content. It uses state-of-the-art AI models for text extraction, image description, and natural language understanding to provide meaningful insights.  

---

### Features
- **OCR-based Text Extraction**: Extracts text from images using Tesseract OCR for text-heavy images.
- **Image Description**: Generates natural language descriptions for visual (non-text) images using BLIP (a vision-language model).
- **Question Answering**: Provides answers to user queries about the extracted text or generated image description using Cohere's large language models.
- **Streamlit Interface**: Interactive user interface for image uploads and chat-based interactions.

---

### How It Works
1. **Upload an Image**: The app accepts image files in `.png`, `.jpg`, or `.jpeg` formats through a sidebar uploader.
2. **Image Analysis**:
   - **Text Classification**: Determines whether the image is text-heavy or natural using heuristics (e.g., amount of detected text).
   - **Text Extraction**: If the image is text-heavy, the app extracts textual data using Tesseract OCR.
   - **Image Description**: For natural images, the app generates captions using BLIP.
3. **Question Answering**: Users can input queries about the image's content, and the app uses Cohere's LLMs to generate responses based on the analyzed content.
4. **Chat Interface**: The conversation is stored and displayed in a chat-like format for a seamless experience.

---

### Installation

#### Prerequisites
- Python 3.8+
- The following Python libraries:
  - `streamlit`
  - `pytesseract`
  - `Pillow`
  - `cohere`
  - `transformers`
  - `pandas`
  - `langchain` and its dependencies

3. Set up Tesseract OCR:
   - Install Tesseract (required for OCR functionality). Instructions can be found [here](https://github.com/tesseract-ocr/tesseract).
   - Ensure Tesseract is in your system's PATH.
4. Set your Cohere API key:
   - Replace `YOUR_API_KEY` in the code with your own Cohere API key.

---


### Code Explanation

#### 1. **Text vs. Natural Image Classification**
The function `classify_image` uses Tesseract OCR to detect text in the image. If significant text is found, the image is classified as "text"; otherwise, it's "natural."

#### 2. **Text Extraction (OCR)**
For text-heavy images, `extract_text_from_image` uses Tesseract OCR to extract text and returns it as a string.

#### 3. **Image Description**
For natural images, `get_image_description` leverages BLIP (Salesforce's image captioning model) to generate a descriptive caption.

#### 4. **Cohere for Question Answering**
The function `qa_with_cohere` creates a prompt using the extracted text or image description and sends it to Cohere's language model to generate a response.

#### 5. **Streamlit Interface**
- **File Upload**: Allows users to upload an image via the sidebar.
- **Image Display**: Displays the uploaded image for user reference.
- **Chat Interface**: Captures user queries and displays AI responses in a chat format.

---

### Output
![image](https://github.com/user-attachments/assets/065dac1f-71cd-456d-894d-3d346b7029fd)
![image](https://github.com/user-attachments/assets/eedaa172-3271-45f4-9796-430614f84f4b)

---

### Dependencies
- **Tesseract OCR**: For text extraction from images.
- **BLIP**: For natural image captioning.
- **Cohere**: For answering questions about the analyzed content.
- **Streamlit**: For building the user interface.

---

### Future Improvements
- Support for multiple languages in OCR.
- Enhanced table extraction capabilities for structured data.
- Integration with additional language models for diverse use cases.
