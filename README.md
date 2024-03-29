# Docker for Perplexity-Inspired LLM Answer Engine 

You can deploy this Docker image on any amd64 machine by following these steps:

Step 1. Pull the Docker Image: 

    ```
    docker pull abhishekkataria16/llm-answer-engine
    ```

Step 2. Create a `.env` file and add your API keys:

    ```
    OPENAI_API_KEY=your_openai_api_key
    GROQ_API_KEY=your_groq_api_key
    BRAVE_SEARCH_API_KEY=your_brave_search_api_key
    SERPER_API=your_serper_api_key
    ```

Step 3. Run Docker with following command:

    ```
    docker run -d -p 3000:3000 -v /path/to/.env:/app/.env  abhishekkataria16/llm-answer-engine
    ```

To run the container via docker compose:

Step 1: Create a docker-compose.yml file with following code:

    ```
    version: '3.8'

    services:
      llm-answer-engine:
        image: abhishekkataria16/llm-answer-engine
        ports:
         - "3000:3000"
        volumes:
         - /path/to/.env:/app/.env
    ```
Step 2: Run the docker compose file via following command:

    ```
     docker-compose up -d

    ```

Original Repo: https://github.com/developersdigest/llm-answer-engine/tree/main