# SciHub Topic Modeling

This repository contains Python scripts and visualisation output for a project that aimed at processing and analyzing a large dataset of scientific papers. We start by processing over 2.4TB of compressed PDF documents from Sci-Hub, extracting valuable metadata and content. After cleaning the data, we classify the papers into study areas based on Scopus categories. Finally, we apply Latent Dirichlet Allocation (LDA) to uncover trending topics within each study area, revealing intriguing insights about the current landscape of scientific research. 

The project uses Apache Tika library for text and metadata extraction from PDF files, scikit-learn library for topic modeling, and PySpark for large-scale data processing.

## Project Structure

This project consists of several Python Notebook (.ipynb) files and a visualisatiion folder with multiple HTML(.html) files representing the output. The Python files are built in the following sequence:

1. **Data Loading (Data Loading.ipynb)**: This file is responsible for loading the dataset, which is expected to be a collection of PDF documents compressed in ZIP files. The metadata and plain text content(including the title, DOI, creation time, subject, and content) are extracted from the PDFs using the Tika library.

2. **Data Cleaning (data-cleaning.ipynb)**: This file cleans and preprocesses the extracted data.

3. **Journal Match (Journal Match-final.ipynb)**: These file classifies each paper into its study area. The journal titles are matched against a table to get their ASJC classification codes, and these classification codes can be used to assign a subject area and sub-discipline to each paper.

4. **LDA Visualization (ldavisual.ipynb)**: These files perform topic modeling using Latent Dirichlet Allocation (LDA) on the preprocessed text data, and visualize the modeling results.

5. **Results Visualization (visualization/)**: This directory contains HTML files for visualizing the final results. 


## Visualization Results

In this project, we use multiple HTML files for visualizing the final LDA results. These files are in the `visualization` directory. 

[The visualisation output also can be previewed here.](http://htmlpreview.github.io/?https://github.com/Qingxian089/SciHub-Topic-Modeling-/blob/master/visualisation/index-2.html)
