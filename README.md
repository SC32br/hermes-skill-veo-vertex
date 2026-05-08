# Hermes Skill: Vertex AI Veo Video Generator 🎬✨

[![Hermes Agent](https://img.shields.io/badge/Hermes-Skill-blue.svg)](https://github.com/NousResearch/hermes-agent)
[![Google Cloud Vertex AI](https://img.shields.io/badge/Vertex%20AI-Veo%203.1-orange.svg)](https://cloud.google.com/vertex-ai)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A powerful skill for [Hermes Agent](https://github.com/NousResearch/hermes-agent) that enables autonomous high-quality video generation using Google's state-of-the-art **Veo (Veo 3.1)** models via Vertex AI.

## 🌟 Features

- **High-Quality Video Generation:** Utilizes Google's Veo 3.1 for cinematic, high-resolution video creation.
- **Autonomous Agent Integration:** Fully compatible with Hermes Agent's multi-step planning and tool-calling.
- **Secure Authentication:** Uses standard Google Cloud credentials (`GOOGLE_APPLICATION_CREDENTIALS`).
- **Automated Storage:** Automatically manages outputs via Google Cloud Storage (GCS).

## 🚀 Installation

You can install this skill directly into your Hermes Agent using the following command:

```bash
hermes skills install https://raw.githubusercontent.com/SC32br/hermes-skill-veo-vertex/main/SKILL.md
```

## ⚙️ Configuration

Ensure you have configured your Google Cloud environment with the necessary permissions:

```bash
export GOOGLE_CLOUD_PROJECT="your-project-id"
export GOOGLE_CLOUD_LOCATION="us-central1"
export VEO_GCS_BUCKET="your-gcs-bucket-name"
export GOOGLE_APPLICATION_CREDENTIALS="/path/to/your/service-account.json"
```

## 🛠️ Usage

Once installed, just ask Hermes:

> *"Hermes, create a cinematic video of a futuristic city using the Veo skill."*

## 📚 Repository Structure
- `SKILL.md` - Main skill documentation and execution instructions for Hermes.
- `scripts/generate.py` - The backend Python script interacting with Vertex AI APIs.
