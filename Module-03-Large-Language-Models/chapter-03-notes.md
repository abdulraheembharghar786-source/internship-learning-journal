
## 📌 Part 1: Large Language Model (LLM) Integration
Focuses on the transition from basic prompting to programmatic API interaction.

### 1.1 API Configuration & Troubleshooting
When switching from **AI Proxy** to **AI Pipe** to resolve `401 Unauthorized` or `Key Expired` errors, two mandatory changes are required in your script:
* **Base URL:** Update the endpoint to the specific Pipe provider URL.
* **API Key:** Replace the Proxy token with the new Pipe-based token.

### 1.2 Secure Secret Management
Hardcoding API keys is strictly prohibited. Use the `os` library to manage secrets securely:

```python
import os

# Securely retrieving the API key from environment variables
api_key = os.getenv("DATA_PIPE_TOKEN")

if not api_key:
    raise ValueError("DATA_PIPE_TOKEN not found in environment variables.")
