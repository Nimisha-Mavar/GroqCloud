# GroqCloud Integration 🎐

### What is GroqCloud?
GroqCloud is a cloud-based inference platform designed to deliver ultra-fast AI model inference with low latency and high performance. It empowers developers to run LLMs (Large Language Models) with blazing-fast speed, making AI applications smoother and scalable.

### Where to Use?
- Real-time chatbot applications 🤖💬
- AI content generation tools
- Video/Audio transcription services
- Image Captioning
- Edge AI applications needing quick responses

### Key Features 🚀
- High-speed inference  
- Scalable cloud architecture  
- Low latency execution  
- Easy API integration  
- Supports popular LLMs like LLaMA, GPT, and more  
- Free tier available with **1000 tokens/month**  

### Implementation
1. **Signup & API Key Generation** 🔑  
   - Visit [GroqCloud](https://groq.com/) and create an account.  
   - Free users get 1000 requests/day and 100,000 tokens/day.  
   - Generate API Key from dashboard under Free Tier.  

2. **Install Dependencies**  
   ```bash
   pip install requests

3. **API Request Example**
```python
import requests

API_KEY = 'your_api_key'
url = 'https://api.groq.com/openai/v1/chat/completions'
headers = {
    'Authorization': f'Bearer {API_KEY}',
    'Content-Type': 'application/json'
}

payload = {
  "model": "mixtral-8x7b-32768",  # Model naam change kari shake
  "messages": [
    {"role": "user", "content": "Hello Kanuda, how can GroqCloud help you today?"}
  ],
  "temperature": 0.7,
  "max_tokens": 100
}

response = requests.post(url, headers=headers, json=payload)
print(response.json()["choices"][0]["message"]["content"])
```
4. **Output Example**
```python
{
   "output": "GroqCloud helps with blazing fast inference for AI models!"
}
```

