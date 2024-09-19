
# Cold Email Generator

This project is designed to scrape job postings from websites and generate structured JSON outputs, making it easier to extract relevant information such as role descriptions, skills, and experience. Using the `LangChain` framework, it leverages large language models to process the raw text.

## Features

- **Web Scraping**: Extracts text data from websites.
- **JSON Output**: Converts job postings into structured JSON with fields like `role`, `experience`, `skills`, and `description`.
- **Natural Language Processing**: Utilizes an LLM (`llama-3.1-70b-versatile`) for understanding and parsing unstructured text.

## Requirements

- Python 3.8+
- Required libraries:
  - `langchain_groq`
  - `langchain_core`
  - `requests` (for web scraping)
  - `beautifulsoup4`

Install the dependencies via pip:

```bash
pip install -r requirements.txt
```

## Usage

1. Clone the repository:

```bash
git clone https://github.com/yourusername/cold_email_generator.git
cd cold_email_generator
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Run the Jupyter Notebook:

```bash
jupyter notebook cold_email_generator.ipynb
```

4. Configure your API key and model name inside the notebook:

```python
llm = ChatGroq(
    temperature=0,
    groq_api_key='your_api_key',
    model_name="llama-3.1-70b-versatile"
)
```

5. Input the data you want to process:

```python
response = llm.invoke("Scraped text or query...")
print(response.content)
```

6. Output the extracted JSON data:

```python
{
    "role": "Lead Full Stack Developer",
    "experience": "Not specified",
    "skills": ["HTML/CSS", "JavaScript", "Node.js", "SQL", "Python"],
    "description": "Responsible for full software development life cycle."
}
```

## File Structure

```
cold_email_generator/
│
├── cold_email_generator.ipynb  # Main Jupyter notebook
├── requirements.txt            # Python dependencies
└── README.md                   # Project documentation
```

## License

This project is licensed under the MIT License.
