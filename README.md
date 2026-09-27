# WhatsApp AI Agent (n8n)

An AI-powered WhatsApp assistant built with n8n. It understands text, voice
messages, and images, and replies naturally using a persistent conversation
memory per user.

## How it works
1. **WhatsApp Trigger** receives an incoming message and a **Switch node**
   routes it based on message type: text, image, or audio.
2. **Voice messages** are downloaded and transcribed to text (Whisper via
   OpenAI) before being passed to the agent.
3. **Images** are downloaded and analyzed (GPT-4.1 vision) to produce a text
   description before being passed to the agent.
4. All three paths converge into one **AI Agent**
