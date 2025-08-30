# PPTGen – Automatic Presentation Generation from Text

PPTGen is a lightweight web application that converts long-form text or markdown into a professionally styled PowerPoint presentation. The application allows users to paste text from various sources such as notes, reports, or general prose and instantly generate a ready-to-present deck. Users can upload their own presentation template and an optional guidance prompt, along with their preferred Large Language Model (LLM) API key to customize the output.

-----

## Key Features

  * **Input Flexibility**: The application accepts large blocks of text, including markdown and prose.
  * **Custom Guidance**: Users can provide a single-line instruction to guide the tone or structure of the presentation, such as "make it an investor pitch deck."
  * **API Key Integration**: It supports various LLM APIs, including OpenAI, Anthropic, and Gemini. User keys are not stored or logged.
  * **Template Customization**: Users can upload their own `.pptx` or `.potx` templates to apply specific colors, fonts, and layouts.
  * **Image Reuse**: The application intelligently incorporates existing images from the uploaded template into the new presentation.
  * **Instant Output**: A new `.pptx` file is generated and available for immediate download.
  * **Smart Content Division**: The system automatically splits the input text into a logical number of slides.
  * **Privacy-Focused**: The application does not log or save any user text, API keys, or uploaded files.

-----

## Getting Started

### 1\. Clone the repository

```bash
git clone https://github.com/shreya-pal/PPTGen.git
cd PPTGen
```

### 2\. Install dependencies

```bash
# Backend (Python FastAPI + pptx libraries)
pip install -r requirements.txt

# Frontend (served as static HTML/JS/CSS)
# No build step is required.
```

### 3\. Run the application locally

```bash
uvicorn app:app --reload
```

Access the application by navigating to `http://localhost:8000`.

### 4\. Deployment

This application is designed to work seamlessly on cloud platforms such as Railway, Render, Vercel, or Heroku. It can be deployed by simply connecting the repository.

-----

## Usage Instructions

1.  Paste your text or markdown into the input field.
2.  Optionally, add a single line of guidance, such as “make it a research summary.”
3.  Provide your LLM API key (OpenAI, Anthropic, or Gemini).
4.  Upload a `.pptx` or `.potx` template.
5.  Click **Generate** to receive your new, styled PowerPoint deck.

-----

## Architectural Overview

  * **Frontend**: Built with responsive HTML and Tailwind UI. It manages user input, template uploads, and file downloads while providing progress feedback and a history of previous generations.
  * **Backend**: Developed using FastAPI. It processes the text, guidance, API key, and template. The backend intelligently splits the content into slide sections and maps the new information to the uploaded template's style, layout, fonts, and images. It generates the final `.pptx` file using `python-pptx`.

-----

## Proposed Enhancements

  * Add automatic generation of speaker notes.
  * Provide a library of pre-built guidance templates (e.g., sales deck, investor pitch, research summary).
  * Implement live slide previews before the final download.
  * Improve error handling and add retry logic for unstable API connections.

-----

## License

This project is released under the MIT License, allowing for free use, modification, and distribution.
