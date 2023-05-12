# AI tools

The tools are like weapons, they are only as good as the person using them. The tools are not a replacement for a good understanding of the any concepts.

> These tools should be used for automating the boring stuff, not for replacing the intelligence of the human.
> Also, learn in the recommendation process.

## Different AI models

### ChatGPT (by OpenAI) | Microsoft

![](img/chatgpt_prompts.png)

## Tools

- [gpt4free](https://github.com/xtekky/gpt4free)
  - it uses multiple models including chatgpt. And it's for free. There are search engines based on GPT4 for free - phind, you.com, and others.
- Prompt Community: https://flowgpt.com/
  - learn prompting from the community's prompts.
- Multiple fields:
  ![](img/ai_tools1.png)
- [Prompt formula with different examples](https://www.linkedin.com/posts/rahulkanotra_chatgpt-activity-7052276853188796416-4vii)
- For coding in VSCode, use this extension: [AI-Genie](https://github.com/ai-genie/chatgpt-vscode)
  > Turn on billing in OpenAI website to get this extension working.
- Image generator
  - [Midjourney](https://www.midjourney.com/)
  - [Hotpot](https://hotpot.ai/)
- Video Summary:
  - [YT Summary Chrome extension](https://chrome.google.com/webstore/detail/youtube-article-summary-p/nmmicjeknamkfloonkhhcjmomieiodli/related)
- [ChatGPT for Google](https://chrome.google.com/webstore/detail/chatgpt-for-google/jgjaeacdkonaoafenlfkkkmbaopkbilf)
- [OpenAI Toolkit - AI Prompt For Social Media](https://chrome.google.com/webstore/detail/openai-toolkit-ai-prompt/acgbggfkaphffpbcljiibhfipmmpboep/related)
  ![](img/ai_tools_social.png)

## Usage

### Coding

- Using the tool `genie` (`chatgpt-vscode`) for getting help for errors in the code. Don't forget to add billing into the OpenAI account.
- Use Copilot (currently based on Codex model) for generating the code.
- Use the AI prompt UI like `chat.openai.com` to generate the code based on prompting.
  > The GUI supports latest model, whereas the VSCode extension supports only chatgpt FREE model.

### Task Management

- Automate **Jira, ClickUp, Shortcut** (or any task management tool) tickets detailing. For instance, you have a title defined, and you want to generate a description for the ticket. You can use the tool (any AI model like ChatGPT) to generate the description.
  > Give more context to the prompt to get better results.

![](img/task_management_ai.png)

<details>
<summary><b>example prompt: </b></summary>

```txt
I need your assistance in creating and setting up Task detailing properly for a [project]

project = "A sophisticated TODO app with Blockchain integration"

I will provide you with title
Please do the following in order to give me accurate detailing:

1. user story description
2. Analyse the story and break it down to Backend, Frontend(UI), Frontend(Integration), Blockchain subtasks
3. Then give me their respective subtasks with their detailed descriptions and acceptance criteria

Here, Frontend(Integration) means the API developed in Backend tasks and UI screens built in Frontend(UI)

I need you to provide the detailing in the following order:

The format should be like this
1. User Story Description
Subtasks
1. Backend
  1.1. Task 1
      1.1.1. Description and acceptance criteria for each tasks and so on
1. Frontend(UI)
      2.1.1. Description and acceptance criteria for each tasks and so on
2. Frontend(Integration)
      3.1.1. Description and acceptance criteria for each tasks and so on
3. Blockchain
      4.1.1. Description and acceptance criteria for each tasks and so on
```

</details>

## Project Ideas

![](img/ai_project_ideas_1.png)

## References

- [Learn Prompting book](https://learnprompting.org/docs/basics/intro)
