# theGraphLLM

# TheGraph-LLM Demo

## Overview
This notebook demonstrates how to extract data via TheGraph and use GPT to create a chatbot-like experience for blockchain data analytics. This requires accounts with both TheGraph and OpenAI.

## Prerequisites
- **TheGraph Account:** You will need a TheGraph API key. [Create an account here](https://thegraph.com/en/).
- **OpenAI Account:** You will need an API key from OpenAI. [Sign up for access here](https://www.openai.com/).

## Setup Instructions
### 1. Clone the Repository
Clone this repository to your local machine or open it in Google Colab.

### 2. Install Required Libraries
Ensure you have the necessary libraries installed:
```bash
pip install requests
pip install llama-index  # For handling large text contexts

Set Environment Variables
Add your API keys to your environment:
export THEGRAPH_API_KEY='your-thegraph-api-key'
export OPENAI_API_KEY='your-openai-api-key'
Configure TheGraph Gateway
Modify the gateway_url in the notebook with your TheGraph gateway URL and API key.

Running the Notebook
Follow the instructions in the notebook to:

Set up your API keys.
Execute GraphQL queries.
Interact with GPT using the extracted data.

Example Query
Here's an example of how you might set up a GraphQL query in the notebook:
query = """
{
  factories(first: 5) {
    id
    poolCount
    txCount
    totalVolumeUSD
  }
  bundles(first: 5) {
    id
    ethPriceUSD
  }
  tokens(first: 20) {
    id
    name
  }
}
"""
Error Handling
If you encounter HTTP errors or other issues, the notebook includes error handling to help diagnose problems.

Visualization
Results from TheGraph queries are printed directly in the notebook for easy visualization and further analysis.
