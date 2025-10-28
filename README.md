# Document AI Chat (with Cohere)

This is a simple, no-backend-needed web app that lets you chat with your documents.

Got a dense PDF, a long research paper, or just a wall of text you need to understand? Upload it, and start asking questions. It's powered by Cohere's awesome `command-r` model to give you grounded, accurate answers based only on the document you provide.

<img width="744" height="518" alt="image1" src="https://github.com/user-attachments/assets/796d8e3d-cbe4-4585-94ad-696cdc5ba0d2" />

## How does it work?

It's a pretty straightforward (but powerful) example of Retrieval-Augmented Generation (RAG), all running in your browser:

1. **Parse:** When you upload a `.pdf` or `.txt` file, the app uses `PDF.js` or a `FileReader` to extract all the text.

2. **Inject:** It then takes that *entire* wall of text and stuffs it into a `SYSTEM` prompt for the Cohere API.

3. **Chat:** Every question you ask is sent to the `command-r` model, which has been instructed to only use the document text from its system prompt to find the answer.

No vector databases, no complex backend. Just a clever prompt and a powerful model.

## Features

* **Chat with your Doc:** A full, stateful chat interface to have a conversation with your file.

* **File Support:** Works with both `.pdf` and `.txt` files.

* **RAG in a Box:** Get answers grounded only in the document's content.

* **Helpful Prompts:** Quick-start buttons for "Summarize," "Key Takeaways," and "Sentiment Analysis."

* **Slick UI:** Built with Tailwind CSS for a clean, modern look.

* **Copy to Clipboard:** Easily copy the AI's responses.

## How to Use

It's a single HTML file, so it's super easy to run.

1. **Get the Code:** Clone this repo or just download the `doc-ai.html` file.

2. **Get your API Key:** Go to [Cohere's website](https://cohere.com/) and grab a free API key.

3. **Open in Browser:** Just double-click the `.html` file to open it locally in Chrome, Firefox, or Safari.

4. **Chat!**

   * Paste in your Cohere API key.

   * Upload your document.

   * Start asking questions!


### Warning

This is a **client-side-only** tool. Your Cohere API key is entered in the browser and sent directly to Cohere's servers.

**Do not** host this on a public website with your API key hard-coded! It's intended for personal, local use.
