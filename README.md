# WhatsApp AI Agent — Production Boilerplate

A backend system for building production-grade WhatsApp 
AI assistants with multi-intent classification, 
conversation memory, and async messaging.

## Stack
- Python / FastAPI
- WhatsApp Business API (Meta Cloud API)
- Redis — conversation memory and session management
- RabbitMQ — async message routing
- PostgreSQL — lead and job storage
- Docker + Kubernetes — containerized deployment
- DigitalOcean — cloud infrastructure

## Features
- Multi-intent classification via LLM (Claude/OpenAI)
- Threaded conversation memory keyed by phone number
- Async job processing via RabbitMQ consumers
- Webhook ingestion and deduplication
- Payment gateway integration hooks
- Overdue notification flows with Redis throttling

## Architecture
Webhook → FastAPI → Intent Classifier → RabbitMQ → 
Consumer → WhatsApp Business API
