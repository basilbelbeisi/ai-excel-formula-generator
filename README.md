# AI Excel Formula Generator: Natural Language to Excel Formulas

## Project Overview
This repository contains the Jupyter Notebook for a project that demonstrates how to build an AI-powered **Excel Formula Generator**. The goal is to translate plain English descriptions into accurate Excel formulas, making spreadsheet automation more intuitive.

## How it Works
The project leverages the power of **Hugging Face's T5-small** transformer model, fine-tuned on a custom-generated dataset. We create thousands of examples by pairing natural language instructions (like "Find the average of column B") with their corresponding Excel formulas (e.g., `=AVERAGE(B:B)`). The fine-tuned T5 model then learns to generate these formulas based on new user inputs.

## Features
* Generates Excel formulas for 10 common functions (SUM, AVERAGE, IF, VLOOKUP, XLOOKUP, etc.).
* Uses a programmatically generated dataset for training.
* Achieves high accuracy (over 80% exact match) on unseen data.
* Built using Python, PyTorch, and Hugging Face Transformers.

## Explore the Full Blog Post
For a detailed step-by-step explanation, deep dives into the code, and a video demonstration, please visit the accompanying blog post:

➡️ **[Read the Full Article on DataSkillBlog.com](https://dataskillblog.com/ai-excel-formula-generator)**

## Limitations
This is a prototype, and as such, it has some simplifications:
* Formulas primarily use entire columns (e.g., `A:A`) rather than specific ranges.
* Conditions (for `IF`, `SUMIF`, etc.) are generally simple numeric comparisons.
* Lookup functions use fixed source columns.
These choices were made to keep the dataset clean for demonstration purposes.

## Future Work
* Expand dataset with more complex conditions and nested functions.
* Integrate with Excel directly (e.g., via an add-in).
* Improve user interface for interactive formula generation.
