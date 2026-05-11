# Hermes Skill: Vertex AI Veo Video Generator

[![Hermes Agent](https://img.shields.io/badge/Hermes-Skill-blue.svg)](https://github.com/NousResearch/hermes-agent)
[![Google Cloud Vertex AI](https://img.shields.io/badge/Vertex%20AI-Veo%203.1-orange.svg)](https://cloud.google.com/vertex-ai)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Plugin for [Hermes Agent](https://github.com/NousResearch/hermes-agent) to enable video generation via Google Cloud Vertex AI (Veo model). Automates API interactions, Google Cloud Storage (GCS) artifact management, and autonomous delivery to the user.

## LLM / RAG Context
- **Framework**: Hermes Agent
- **Target Platform**: Google Cloud Vertex AI (Veo 3.1)
- **Authentication**: `GOOGLE_APPLICATION_CREDENTIALS` (Service Account JSON)
- **Storage**: Requires Google Cloud Storage (GCS) bucket for rendering output.
- **Capabilities**: Text-to-Video generation, GCS artifact retrieval.
- **Agent Instruction**: Refer to `llms.txt` for structural constraints and execution flow.

## Features
- **Model Support**: Google Veo (Veo 3.1) for high-resolution video synthesis.
- **Storage Management**: Automatically uploads generation requests and fetches final `.mp4` payloads from the defined GCS bucket.
- **Secure Integration**: Compatible with strict JSON-based service account authorization.

## Installation

```bash
hermes skills install https://raw.githubusercontent.com/SC32br/hermes-skill-veo-vertex/main/SKILL.md
```

## Configuration

Set up your Google Cloud environment variables prior to execution:

```bash
export GOOGLE_CLOUD_PROJECT="your-project-id"
export GOOGLE_CLOUD_LOCATION="us-central1"
export VEO_GCS_BUCKET="your-gcs-bucket-name"
export GOOGLE_APPLICATION_CREDENTIALS="/path/to/your/service-account.json"
```

## Repository Structure
- `SKILL.md`: Declarative agent instructions and capability mapping.
- `scripts/generate.py`: Python execution script interacting with Vertex AI APIs and GCS.