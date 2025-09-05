# 🛒 Product Pages Webscraper with AI (n8n)

This project is an **intelligent webscraper** built with [n8n](https://n8n.io/).  
It collects product page data, transforms it into structured JSON using AI, and stores the results in a database for further analysis.

## ⚙️ Workflow Overview

The workflow works as follows:

1. **Receive URL**  
   The user submits a product page URL through a form (`On form submission`).

2. **Page Scraping**  
   The workflow uses the [Jina.ai](https://jina.ai/) API to scrape the raw content from the product page (`HTTP Request`).

3. **Transform to JSON with AI**  
   The raw data is passed to an **OpenAI Agent**, which converts it into structured JSON (`AI Agent`).  
   - If an error occurs, the agent returns a readable error message.

4. **Python Formatting**  
   A Python script cleans unnecessary characters, validates, and formats the JSON to ensure consistency (`Code`).

5. **Database Storage**  
   The processed data is stored in a relational database for further use (`Insert rows in a table`).


---

## 🚀 How to Use

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/product-pages-webscraper.git
Import the workflow into n8n:

Open n8n.

Click Import workflow.

Upload the workflow.json file.

Configure required credentials:

Jina.ai API Key

OpenAI API Key

Database connection (PostgreSQL, MySQL, etc.)

Run the workflow and submit a product URL through the form.

🧩 Tech Stack
n8n – Automation and workflow orchestration

Jina.ai – Web scraping and parsing

OpenAI – JSON structuring via AI

Python (in n8n Code node) – Data cleaning and formatting

Relational Database – Structured data storage

💡 Future Improvements
Add more robust error handling

Support multiple URLs at once

Export results to Google Sheets or a Data Warehouse

Create dashboards with Power BI / Metabase


✨ Author
Project developed by Victor Souza.