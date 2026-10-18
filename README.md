# Workbot 🤖

Workbot is a Slack productivity bot built to make everyday work easier. It helps turn long messages, rough notes, and project updates into clear summaries and actionable information directly inside Slack.

I built Workbot to explore how AI can be used to solve real workplace problems, reduce repetitive tasks, and help people organize their work without switching between multiple tools.

## What can Workbot do?

Workbot includes several slash commands, each designed for a different task.

### `/workbot-summarize`

Summarizes long messages, notes, and updates into a shorter, easier-to-read format.

It organizes the response into:
- Summary
- Key Takeaways
- Next Steps
- Missing Information, when needed

### `/workbot-actions`

Helps identify action items from a message or a set of notes. It can organize tasks, owners, deadlines, and priorities when that information is available in the original text.

### `/workbot-meeting`

Turns rough meeting notes into organized meeting minutes, including important discussion points, decisions, and follow-up actions.

### `/workbot-draft`

Helps write professional emails, Slack messages, and other workplace communications. It can turn rough ideas into clearer messages while keeping the intended meaning.

### `/workbot-plan`

Helps break a project or goal into smaller steps. It can suggest a structured plan with tasks, milestones, and dependencies based on the information provided.

### `/workbot-status`

Organizes project updates into a status report, highlighting completed work, ongoing tasks, upcoming work, and blockers when the input includes those details.

### `/workbot-ping`

Checks whether Workbot is responding and helps confirm that the bot is running.

### `/workbot-help`

Displays the available commands and explains what each one does.

## How it works

Workbot uses Slack slash commands to receive requests. When someone runs a command, the bot processes the supplied text and sends it to an AI model through the Groq API.

The AI generates a response based on the task requested, and Workbot returns the result in Slack. This makes it possible to summarize information, organize tasks, and draft messages without leaving the workspace.

Workbot also follows specific instructions to keep responses concise and professional. It is designed not to invent task owners, deadlines, decisions, or other details that were not provided.

## Technologies used

- **JavaScript / Node.js** — the main application runtime
- **Slack Bolt for JavaScript** — handles Slack commands and bot interactions
- **Groq API** — powers the AI features
- **Axios** — sends HTTP requests to the AI API
- **dotenv** — loads environment variables from a local `.env` file

## Project structure

The main application logic is in `index.js`, which handles the Slack commands, sends requests to the AI API, and returns responses to Slack.

The `.env` file stores local credentials and configuration. It should remain private and must not be uploaded to the public repository.

## A few things to know

- Workbot needs a working internet connection to communicate with Slack and Groq.
- AI responses may occasionally need review or correction.
- Missing information is identified rather than automatically filled in with invented details.
- Workbot can only access information that is provided to it or made available through configured integrations.
- API availability, model access, and usage limits may affect AI features.

## Future improvements

There are plenty of ways to expand Workbot, including better task formatting, more detailed project reports, integrations with other productivity tools, and additional commands for everyday team workflows.

## Why I built it

I wanted to build something practical that combines software development, APIs, and AI. Workbot gave me a chance to work with Slack integrations and learn how to connect an AI model to an application that people can use for everyday tasks.

The goal is simple: spend less time organizing information manually and more time getting work done.

