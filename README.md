# Slides Assistant
**Your AI-Powered Presentation Partner**

## What is Slides Assistant?
Slides Assistant is an AI application designed to streamline the process of generating ideas and crafting PowerPoint presentations. Whether you're preparing for a business meeting, a class presentation, or a conference talk, Slides Assistant is here to help you create professional presentations effortlessly.

## Technology Stack
Slides Assistant utilizes [Chainlit](https://chainlit.io/) for the front-end interface and OpenAI or Azure OpenAI APIs at the backend. It leverages the latest GPT model (GPT-4o) and function calling (tools) to enhance its capabilities. Additionally, the python-pptx library is used to create the PowerPoint files.

## Instructions:
- Clone the source code:
```bash
git clone https://github.com/skydockAI/slides_assistant.git
```

- Build the Docker image:
```bash
docker build -t slides_assistant:latest .
```

- Configure Environment Variables: Open the [config.env](config.env) file and update **OPENAI_KEY** (if you use OpenAI) or **AZURE_OPENAI_KEY**, **AZURE_OPENAI_ENDPOINT** and **AZURE_OPENAI_VERSION** (if you use Azure OpenAI).

- Run the Docker image:
```bash
docker run --env-file ./config.env -p 8000:8000 slides_assistant:latest
```

- Open [http://localhost:8000/](http://localhost:8000/) to start using the Slides Asisstant application. 

## Screenshots
<img src="/images/step_1.png" alt="Propose ideas for presentation topic"></img>

<img src="/images/step_2.png" alt="Adjust length of presentation slides"></img>

<img src="/images/step_3.png" alt="Confirm to create PowerPoint file"></img>

<img src="/images/generated_slides.png" alt="Generated slides"></img>

The generated PowerPoint file in the example above can be downloaded [here](/examples/The_History_Of_Canada.pptx)

## License:
**Slides Assistant** is open-source and licensed under the [GPL-3.0](LICENSE) license.
