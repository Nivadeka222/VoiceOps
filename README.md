# VoiceOps – AI Voice Support Platform

VoiceOps is an AI-powered voice support backend that automates customer interactions by combining speech recognition, large language models, and text-to-speech processing.

## Features

- **Voice Processing:** Integrates Speech-to-Text, LLM-based response generation, and Text-to-Speech.
- **Priority Queue Management:** Uses Redis-backed priority queues to manage incoming calls.
- **Scheduled Jobs:** Supports scheduled task execution and retry handling.
- **Failure Handling:** Implements retry mechanisms, failure recovery, and dead-letter processing.
- **Real-Time Monitoring:** Uses WebSockets to track call status, queue depth, retries, latency, and human handoffs.
- **Event Logging:** Maintains structured logs for tracking system events and failures.

## Tech Stack

- **Backend:** Python, FastAPI
- **Queue Management:** Redis
- **Real-Time Communication:** WebSockets
- **AI Integration:** LLM, Speech-to-Text, Text-to-Speech

## Architecture

1. Incoming voice requests enter the FastAPI backend.
2. Speech-to-Text converts audio into text.
3. The LLM processes the input and generates a response.
4. Text-to-Speech converts the response into audio.
5. Redis manages queued and scheduled tasks, including retries and failed jobs.
6. WebSockets provide real-time updates to the monitoring dashboard.

## Project Status

Core backend components include voice-processing integration, Redis-based queue management, failure handling, and real-time monitoring.
