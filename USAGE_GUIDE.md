# GTM Canvas Skill Usage Guide

This guide explains how to integrate and use the `gtm-canvas` skill in your preferred AI platform.

## 1. Claude Projects (Recommended)
Claude Projects allow you to upload the `SKILL.md` file and reference files as "Knowledge" to provide a consistent experience.

1.  **Create a Project**: Go to Claude.ai and create a new project.
2.  **Upload Knowledge**:
    - Upload `SKILL.md`.
    - Upload the `knowledge/` and `resources/` folders if you have them.
3.  **Update Instructions**: 
    - Copy the contents of `SKILL.md` into the **"Project Instructions"** (System Prompt) field.
4.  **Initiate**: Start a new chat and say: "I want to create a GTM Strategy using GTM Canvas."

## 2. OpenAI Custom GPTs
You can build a specialized GPT to act as your GTM facilitator.

1.  **GPT Builder**: Go to ChatGPT and select "Create a GPT".
2.  **Configure**:
    - **Instructions**: Paste the full text from `SKILL.md` into the Instructions box.
    - **Knowledge**: Upload all files from the `knowledge/`, `resources/`, and `examples/` directories.
3.  **Capabilities**: Ensure "Web Browsing" and "Code Interpreter" are enabled if desired (though not strictly required for the core framework).

## 3. Cursor / Windsurf / Continue.dev
These IDE extensions support local skills and agents.

1.  **Project Root**: Ensure the `gtm-canvas-skill` folder is in your repository.
2.  **Indexing**: 
    - For **Cursor**, the AI naturally indexes files in your project. You can `@SKILL.md` to give it the context before starting.
    - For **Windsurf** or **Continue**, ensure the `.agent/skills/` directory structure is respected if applicable to your configuration.
3.  **Trigger**: Simply mention "GTM strategy" or "GTM Canvas" in the chat window while the files are indexed.

## 4. Raw API / Developer Frameworks
If you are building your own agent using LangChain, LlamaIndex, or raw API calls:

- **System Message**: Send the entire content of `SKILL.md` as the `system` message in your Chat completion request.
- **Tools**: If your framework supports tools/skills folders, point it to this directory.
- **RAG**: For larger resource files (like the handbook), use a RAG (Retrieval-Augmented Generation) pipeline to fetch relevant data when the user asks specific questions.

---

## Tips for Best Results
- **One Step at a Time**: The facilitator is designed to be conversational. If the AI tries to rush, remind it: "Let's focus on Component 1 first."
- **Iterative Thinking**: The GTM Canvas is a living document. Re-run the facilitation every 2 weeks to update your strategy based on market feedback.
- **Use Examples**: If you get stuck on a section like "Alpha", ask the AI: "Can you show me an example of an Alpha for a SaaS product?"
