---
author: Aryan
title: UGC Video Creator — Agentic AI System for Content Generation
date: 2025-12-08
description: A brief description of Hugo Shortcodes
---
**UGC Video Creator** is an **agentic AI-powered content generation system** that transforms a single reference image into **brand-safe UGC-style images and short-form videos**.  
The system is designed to handle **real-world content constraints**, including brand safety, pose variation, identity consistency, and platform compliance.

🔗 **GitHub:** https://github.com/AryanManojKumar/UGC_video_creator  

---

### Core Capabilities

**Agentic AI Architecture**
- Central **orchestrator agent** routes tasks to specialized agents  
- Modular agent design allows independent reasoning and validation steps  
- Agents operate under strict system instructions to enforce constraints  

**Multi-Agent Workflow**
- **Prompt Generation Agent:** Converts high-level intent into model-ready prompts  
- **Prompt Variator Agent:** Generates pose and framing variations while preserving identity  
- **Safety & Compliance Agent:** Enforces brand safety, content restrictions, and placement rules  
- **Script & Dialogue Validator:** Ensures dialogue and lip-sync inputs comply with platform and product constraints  

**UGC Image & Video Generation**
- Generates multiple image variants from a single reference image  
- Supports **image-to-video pipelines** for short-form UGC clips  
- Designed for silent or lip-sync-compatible video outputs  

---

### Real-World Constraints Handled

- Identity preservation across generations  
- Product placement below face level (no mouth or lip overlap)  
- Brand-safe framing and behavior enforcement  
- Platform-specific constraints (short duration, vertical format)  
- Cost and latency trade-offs across different generative models  

---

### System Architecture Overview

- **Input Layer:** User intent + reference image  
- **Orchestration Layer:** LLM-based master agent controlling task flow  
- **Agent Layer:** Specialized agents for prompting, variation, safety, and validation  
- **Generation Layer:** Image and video generation models 
- **Post-Processing Layer:** Script checks, lip-sync readiness, and output validation  

This layered design enables **safe iteration**, **parallel execution**, and **scalability**.

---

### Tech Stack

- **Languages:** Python  
- **LLMs:** OpenAI / Gemini models (prompt reasoning & orchestration)  
- **Vision Models:** Image generation and image-to-video models ( nano_banana , veo3)
- **Audio & Lip Sync:** TTS and lip-sync pipelines (optional)  (elevenlabs , sync_lipsync)  
- **Workflow:** Agent-based orchestration (Crew-style architecture)  
- **Deployment:** API-driven, cloud-ready pipelines  

---

### What This Project Demonstrates

- Designing **agentic AI systems** with multiple cooperating agents  
- Enforcing **safety and compliance** in generative AI pipelines  
- Integrating **multimodal models** (LLMs, vision, video, audio)  
- Handling **production constraints** like latency, cost, and determinism  
- Building AI systems beyond single-prompt generation  

---
