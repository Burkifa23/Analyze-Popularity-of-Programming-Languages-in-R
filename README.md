# Analyze Popularity of Programming Languages
ToDO: Use the updated StackOverFlow Data

An R-based data analysis project that examines the popularity trends of programming languages and technologies using Stack Overflow question data from 2008-2020.

## Overview

This project uses Stack Overflow question tags as a proxy for measuring the popularity of different programming languages and technologies. By analyzing the frequency and trends of questions tagged with specific technologies, we can identify which languages are most widely used and how their popularity has changed over time.

## Dataset

The analysis uses `stack_overflow_data.csv`, which contains Stack Overflow question data with the following structure:

| Column | Description |
|--------|-------------|
| `year` | The year the question was asked (2008-2020) |
| `tag` | A word or phrase describing the topic (e.g., programming language) |
| `num_questions` | The number of questions with that tag in that year |
| `year_total` | The total number of questions asked in that year |

**Dataset size:** 420,066 observations

## Key Analysis Questions

### 1. R Language Popularity
- **Question:** What percentage of total questions in 2020 had the "r" tag?
- **Answer:** 0.966% of all Stack Overflow questions in 2020 were tagged with "r"
- **Visualization:** Line plot showing R's percentage trend from 2008-2020

### 2. Top Programming Languages (2015-2020)
- **Question:** What were the five most asked-about tags between 2015-2020?
- **Answer:** 
  1. JavaScript
  2. Python
  3. Java
  4. Android
  5. C#
- **Visualization:** Multi-line plot comparing the popularity trends of these top 5 tags

## Technologies Used

- **Language:** R (version 4.2.1)
- **Libraries:**
  - `readr` - Data import
  - `dplyr` - Data manipulation and transformation
  - `ggplot2` - Data visualization

## Project Structure

```
.
├── notebook.ipynb              # Main analysis notebook
├── stack_overflow_data.csv     # Primary dataset
├── by_tag_year.csv            # Additional data file
├── prog_lang.jpg              # Header image
└── README.md                  # This file
```

## Getting Started

### Prerequisites

Ensure you have R installed with the following packages:

```r
install.packages(c("readr", "dplyr", "ggplot2"))
```

### Running the Analysis

1. Open `notebook.ipynb` in Jupyter Notebook with an R kernel, or RStudio
2. Run all cells sequentially to:
   - Load the dataset
   - Calculate percentage metrics
   - Generate visualizations
   - View analysis results

## Key Findings

- **R Language Trend:** The analysis tracks R's popularity as a percentage of total Stack Overflow questions over time
- **Dominant Languages:** JavaScript, Python, and Java consistently rank as the most discussed technologies
- **Mobile Development:** Android's presence in the top 5 highlights the significance of mobile development
- **Enterprise Languages:** C# maintains strong representation, reflecting its enterprise adoption

## Methodology

1. **Data Loading:** Import Stack Overflow question data using `readr`
2. **Percentage Calculation:** Calculate each tag's percentage of total questions per year
3. **Filtering & Aggregation:** Use `dplyr` to filter specific tags and aggregate data across years
4. **Visualization:** Create line plots with `ggplot2` to show trends over time

## Data Source

Data sourced from the [Stack Exchange Data Explorer](https://data.stackexchange.com/), which provides public access to Stack Overflow's question database.

## Visualizations

The notebook generates two primary visualizations:

1. **R Language Trend (2008-2020):** Single-line plot showing R's percentage over time
2. **Top 5 Languages Comparison (2015-2020):** Multi-colored line plot comparing JavaScript, Python, Java, Android, and C#

## License

This project is for educational and analytical purposes.

## Acknowledgments

- Stack Overflow for providing public access to their data
- Stack Exchange Data Explorer for data accessibility

