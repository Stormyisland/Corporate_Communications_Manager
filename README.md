# Corporate_Communications_Manager
Corporate Communications Manager persona in .json format
# Corporate Communications Manager AI Persona

## Overview
This persona configures an AI assistant as **Jordan Taylor**, a seasoned Corporate Communications Manager. Use this persona to simulate, train, or automate corporate communications tasks — from drafting press releases to managing internal change comms and crisis responses.

## Files
- `corporate_comms_manager.json` – Persona definition (compatible with many AI platforms)
- `README.md` – This file

## Persona Summary
- **Name:** Jordan Taylor
- **Role:** Corporate Communications Manager
- **Style:** Professional, measured, stakeholder-aware
- **Core focus:** Reputation management, clear messaging, risk mitigation

## Use Cases
1. **Drafting communications** – Press releases, CEO emails, intranet posts, talking points
2. **Crisis simulation** – Roleplay a data breach, product recall, or layoff announcement
3. **Internal comms planning** – Town hall scripts, Slack announcements, manager toolkits
4. **Media query response** – Draft holding statements or Q&As
5. **Training** – Teach new comms hires how to think through messaging scenarios

## How to Use
### Option A: With an LLM frontend (e.g., SillyTavern, OpenWebUI)
- Copy the `.json` content into a new character/persona file
- Load the persona before starting a conversation

### Option B: With ChatGPT (custom GPT or API)
- Use the `system_prompt` field as the custom instruction
- Add the persona attributes to the conversation context

### Option C: With Python (OpenAI/Anthropic API)
```python
import json

with open('corporate_comms_manager.json') as f:
    persona = json.load(f)

response = openai.ChatCompletion.create(
    model="gpt-4",
    messages=[
        {"role": "system", "content": persona["system_prompt"]},
        {"role": "user", "content": "Draft a quick holding statement for a possible data leak."}
    ]
)
