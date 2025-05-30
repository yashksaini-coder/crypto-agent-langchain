# Trench AI Local Development Setup Guide

## 1. Clone the Repository

```sh
git clone <your-repo-url>
cd trench-ai
```

---

## 2. Install Python & Dependencies

- Make sure you have **Python 3.10+** (3.12 recommended).
- Install dependencies:

```sh
pip install -r requirements.txt
```

---

## 3. Set Environment Variables

Create a `.env` file in your project root (or set these in your shell).

**Required environment variables:**

| Variable              | Description                                      | Example/Default                      |
|-----------------------|--------------------------------------------------|--------------------------------------|
| `GOOGLE_API_KEY`      | Google Generative AI API key                     | (your key)                           |
| `RAPIDAPI_KEY`        | RapidAPI key for crypto news/search              | (your key)                           |
| `RAPIDAPI_HOST`       | RapidAPI host for crypto news/search             | crypto-news51.p.rapidapi.com         |
| `TWEETSCOUT_API_KEY`  | TweetScout API key for Twitter tool              | (your key)                           |
| `TAVILY_API_KEY`      | Tavily API key for web search                    | (your key)                           |
| `EXA_API_KEY`         | Exa API key for Exa web search                   | (your key)                           |
| `REDIS_HOST`          | Redis host                                       | localhost                            |
| `REDIS_PORT`          | Redis port                                       | 6379                                 |
| `REDIS_DB`            | Redis DB index                                   | 0                                    |
| `REDIS_PASSWORD`      | Redis password                                   | (blank by default)                   |
| `LOG_LEVEL`           | Logging level                                    | INFO                                 |
| `CACHE_TTL`           | Cache time-to-live (seconds)                     | 86400 (24h)                          |
| `CRON_INTERVAL`       | Cache update interval (minutes)                  | 60                                   |
| `API_RATE_LIMIT`      | API rate limit                                   | 100                                  |

**Example `.env` file:**
```
GOOGLE_API_KEY=your_google_api_key
RAPIDAPI_KEY=your_rapidapi_key
TWEETSCOUT_API_KEY=your_tweetscout_key
TAVILY_API_KEY=your_tavily_key
EXA_API_KEY=your_exa_key
REDIS_HOST=localhost
REDIS_PORT=6379
REDIS_DB=0
REDIS_PASSWORD=
LOG_LEVEL=INFO
CACHE_TTL=86400
CRON_INTERVAL=60
API_RATE_LIMIT=100
```

---

## 4. Start Redis (Required for Caching)

Make sure you have a Redis server running locally or accessible at the host/port you set above.

- **Install Redis:**  
  - On Mac: `brew install redis`
  - On Ubuntu: `sudo apt-get install redis-server`
  - On Windows: [Download from here](https://github.com/microsoftarchive/redis/releases)
- **Start Redis:**  
  ```sh
  redis-server
  ```

---

## 5. Run the Application

```sh
python main.py
```

- This will:
  - Start the FastAPI server (default: http://localhost:8000)
  - Start a background scheduler to keep the cache fresh

---

## 6. (Optional) Run with Docker

If you prefer Docker:

```sh
docker build -t trench-ai .
docker run --env-file .env -p 8000:8000 trench-ai
```

---

## 7. Test the API

- You can send requests to the FastAPI server (see `README.md` for sample input/output).
- Example:
  ```sh
  curl -X POST http://localhost:8000/your-endpoint -H "Content-Type: application/json" -d '{"query": "web3 tools"}'
  ```

---

## 8. Troubleshooting

- **Missing API keys:** Make sure all required keys are set in your `.env`.
- **Redis errors:** Ensure Redis is running and accessible.
- **Dependency errors:** Run `pip install -r requirements.txt` again.
- **Port conflicts:** Change the port in `main.py` or Docker if needed.

---

## 9. Extra: Test Individual Tools

You can test tools like `TavilySearchTool` or `ExaSearchTool` with a script like:

```python
import asyncio
from src.tools.tavily_search_tool import TavilySearchTool

async def main():
    tool = TavilySearchTool()
    params = {"query": "web3 tools", "limit": 5}
    result = await tool.execute(params)
    print(result)

if __name__ == "__main__":
    asyncio.run(main())
```

---

**You are now ready to develop and run Trench AI locally!**
If you need more details on endpoints or tool usage, see the `README.md` or ask for specific examples.
