# PPTGen – Auto-Generate a Presentation from Text

**Your Text, Your Style – Turn bulk text or markdown into a polished PowerPoint presentation.**

PPTGen is a lightweight web app that lets you paste long-form text (markdown, prose, notes, reports) and instantly convert it into a styled, ready-to-present PowerPoint deck. Simply upload your own template, add optional guidance, and supply your preferred LLM API key; the app will handle the rest.

-----

## Features

  * **Input Options**: Paste large chunks of text, markdown, or prose.
  * **Guidance**: Add a one-line instruction for tone or structure (e.g., “make it an investor pitch deck”).
  * **Bring Your Own API Key**: Supports OpenAI, Anthropic, Gemini, and more (keys are never stored or logged).
  * **Template Reuse**: Upload your `.pptx` or `.potx` template to apply colors, fonts, and layouts.
  * **Image Reuse**: Recycles existing images from your uploaded template.
  * **Instant Download**: Outputs a new `.pptx` file you can download directly.
  * **Smart Splitting**: Automatically divides your text into a reasonable number of slides.
  * **Privacy First**: No logging or saving of user text, keys, or files.

-----

## 🖥️ Usage

1.  Paste your text or markdown into the app.
2.  (Optional) Add a one-line guidance, such as “make it a research summary”.
3.  Paste your LLM API key (OpenAI, Anthropic, Gemini).
4.  Upload a `.pptx` or `.potx` template.
5.  Click **Generate** to get your styled PowerPoint deck.

-----

## 🛠️ Architecture

  * **Frontend**:

      * Responsive HTML, JS, and CSS.
      * Handles text input, template upload, and file download.
      * Provides progress feedback, notifications, and history of past generations.

  * **Backend (FastAPI)**:

      * Accepts text, guidance, API key, and a template file.
      * Splits the input intelligently into distinct slide sections.
      * Maps new content onto the uploaded template’s style, layout, fonts, and images.
      * Generates the `.pptx` output using the `python-pptx` library.

-----

## 📄 License

This project is licensed under the MIT License, making it free to use, modify, and share.
