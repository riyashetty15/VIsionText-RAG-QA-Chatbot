# Image-QA-RAG-Chatbot
This repository contains the code for an Image QA (Question Answering) RAG (Retrieval-Augmented Generation) Chatbot built using Streamlit, Cohere, and BLIP (Bootstrapped Language-Image Pre-training). The chatbot allows users to upload an image, generates a description of the image, and then answers questions about the image based on the generated description.
<br>
<br>
## Features
<ul><b> Image Upload </b>: Users can upload images in PNG, JPG, or JPEG formats.</ul>
<ul><b>Image Description</b>: The chatbot uses BLIP to generate a description of the uploaded image.</ul>
<ul><b>Question Answering</b>: Users can ask questions about the image, and the chatbot uses Cohere to generate answers based on the image description.</ul>
<ul><b>Streamlit Interface</b>: A user-friendly interface built with Streamlit.</ul>

## Pre-Requisites
<li>Python 3.7 or higher</li>
<li>Streamlit</li>
<li>Cohere API Key</li>
<li>BLIP (Bootstrapped Language-Image Pre-training)</li>

## Key Components
- **Image Description**: Uses BLIP to generate a description of the uploaded image.
- **Question Answering**: Uses Cohere to generate answers based on the image description.
  
### Streamlit UI
- **File Uploader**: Allows users to upload an image file.
- **Image Display**: Displays the uploaded image on the Streamlit app.
- **Image Analysis**: Extracts and displays the image description.
- **Question Input**: Provides a text input for users to ask questions about the image.
- **Response Display**: Shows the AI-generated response to the user's question.

This code sets up a Streamlit application that allows users to interact with an AI chatbot capable of analyzing images and answering questions about them. The main components include image processing, language generation, and a user-friendly interface.
