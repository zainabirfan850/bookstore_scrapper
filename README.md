# Bookstore Intelligence Mission: Web Scraper

A Python web scraper that turns the practice website [books.toscrape.com](https://books.toscrape.com/) into a clean business dataset and uses it to answer pricing and inventory questions.

## What it does
- Scrapes all 50 catalogue pages (1,000 books) using a reusable function and a loop
- Collects Title, Price, Rating (converted from words to 1-5), Availability and product URL
- Saves the data as `competitor_books.csv`
- Answers 7 business questions, a recommendation question and a £100 budget-optimization challenge

## Libraries used
`requests`, `beautifulsoup4`, `pandas`, `numpy`, `matplotlib`

## How to run
1. Install the libraries: `pip install requests beautifulsoup4 pandas numpy matplotlib`
2. Open `scraper.ipynb` in VS Code or Jupyter and choose **Run All**
3. The notebook creates `competitor_books.csv` and `rating_counts.png`

## Key findings (1,000 books)
- Most expensive: *The Perfect Play (Play by Play #1)*, £59.99
- Cheapest: *An Abundance of Katherines*, £10.00
- Average price: £35.07
- 5-star books: 196 (19.6%)
- In stock: 100%
- Average price is almost the same for every rating (£34.56 for 1-star, £35.37 for 5-star), so high quality does not cost more
- £100 challenge: 9 books, total cost £99.76, total rating score 44 (solved with knapsack optimization)

## Files
- `scraper.ipynb`: scraper and analysis
- `competitor_books.csv`: scraped dataset
- `rating_counts.png`: bar chart of books per star rating

*The website is a sandbox: its prices and ratings were randomly assigned, so the findings describe the dataset, not real customer demand.*