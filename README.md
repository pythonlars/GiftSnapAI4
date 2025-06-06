# GiftSnap - AI Gift Recommendation System

A simple AI-powered gift recommendation system that helps you find the perfect gift for your friends and family based on their profiles and your preferences.

## Setup

1. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

2. Create a `.env` file in the `Data_Base` folder with your API key:
   ```
   GIFTSNAP_API_KEY=your_groq_api_key_here
   ```

## How to Use

The system works in 4 simple steps:

### 1. Create Your User Profile

Run:
```
python code/UserDataColescting.py
```

This will ask for your basic information and save it to `Data_Base/UserData.txt`.

### 2. Create a Gift Recipient Profile

Run:
```
python code/gifting_profiel_generate.py
```

This will ask for information about the person you want to buy a gift for and save it to the appropriate location.

### 3. Generate a Prompt

Run:
```
python code/main.py
```

This will ask which person you want to find a gift for, your budget, and creativity level. It will generate a prompt and save it to `Prompt.txt`.

### 4. Generate Gift Recommendations

Run:
```
python aiBakend.py
```

This will use the Groq API to generate gift recommendations based on your prompt and save the results to `output.txt`.

## Features

- 🎁 AI-powered personalized gift recommendations
- 🔒 Secure API key management with environment variables
- 🤖 Powered by LLaMA 3 70B model via Groq API

## Prerequisites

- Python 3.8+
- Groq API key (Get one from [Groq](https://console.groq.com/))

## System Components

1. `code/UserDataColescting.py` - Creates your personal user profile
2. `code/gifting_profiel_generate.py` - Creates profiles for gift recipients
3. `code/main.py` - Generates the prompt based on profiles and preferences
4. `aiBakend.py` - Processes the prompt with AI and generates recommendations

## Environment Variables

| Variable | Required | Description |
|----------|----------|-------------|
| `GIFTSNAP_API_KEY` | Yes | Your Groq API key |

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [Groq](https://groq.com/)
- [LLaMA 3](https://ai.meta.com/llama/)
