# Dell Laptops Web Scraper

This project is a Jupyter Notebook-based scraper that collects details of Dell laptops, including their names and processor specifications, from Dell's website. It uses the following Python libraries for web scraping and execution:

- `requests`
- `beautifulsoup4`
- `ipykernel`

## Features

- Scrapes multiple pages of Dell's laptops section dynamically.
- Collects laptop names and processor specifications into a structured format.
- Automatically stops when no more laptops are available.

## Requirements

Ensure you have the following Python libraries installed:

- `requests`
- `beautifulsoup4`
- `ipykernel`
- `notebook`

## Setting Up the Virtual Environment

1. Create a virtual environment:
   ```bash
   python -m venv venv
   ```
2. Activate the virtual environment:
   - On Windows:
     ```bash
     venv\Scripts\activate
     ```
   - On macOS/Linux:
     ```bash
     source venv/bin/activate
     ```
3. Install the dependencies:
   ```bash
   pip install requests beautifulsoup4 ipykernel notebook
   ```

## How It Works

1. The script starts at page 1 of Dell's laptops section.
2. Fetches the page content using an HTTP GET request.
3. Parses the content with BeautifulSoup to extract product details:
   - Laptop Name
   - Processor Specification
4. Automatically continues to the next page until no laptops are found.
5. Extracted details are stored in a Python list for further use.

## How to Run

1. Activate your virtual environment (see the steps above).
2. Open the Jupyter Notebook (`laptop_scrap.ipynb`) in your Jupyter environment:
   ```bash
   jupyter notebook laptop_scrap.ipynb
   ```
3. Execute the cells sequentially to run the scraper.
4. The extracted laptop details will be displayed at the end of the notebook.

## Example Output

### Console Output
```plaintext
No laptops available on this page. Exiting loop.
Laptop details collected: [{'laptop': 'Dell Inspiron 15', 'processor': 'Intel Core i7'}, {'laptop': 'Dell XPS 13', 'processor': 'Intel Core i5'}]
```

### Data Structure
The script collects details in the following format:
```python
[
    {'laptop': 'Laptop Name 1', 'processor': 'Processor Details 1'},
    {'laptop': 'Laptop Name 2', 'processor': 'Processor Details 2'},
    ...
]
```

## Notes

- The script assumes the webpage structure remains consistent. If the website layout changes, you may need to modify the notebook.
