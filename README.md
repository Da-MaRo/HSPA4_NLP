# NLP Project for HSPA4-Related Research Papers

Welcome to the NLP Project repository! This project is focused on extracting, processing, and analyzing abstracts from PubMed related to HSPA4, a protein associated with protein quality control. The goal is to identify significant medical labels and genes linked to various cellular processes. Below, you'll find an overview of the project, including setup instructions, usage, and details on how the data is processed.

## Table of Contents

- [Project Overview](#project-overview)
- [Installation](#installation)
- [Usage](#usage)
- [Data Processing Workflow](#data-processing-workflow)
- [Analysis and Results](#analysis-and-results)
- [Contributing](#contributing)
- [License](#license)

## Project Overview

This project leverages natural language processing (NLP) techniques to:

1. **Scrape** abstracts from PubMed for papers related to HSPA4.
2. **Preprocess** the extracted text to prepare it for analysis.
3. **Analyze** the text to identify medical labels and relevant genes associated with protein quality control.

The main tools used in this project include:

- **Beautiful Soup**: For web scraping PubMed abstracts.
- **NLTK**: For text preprocessing.
- **BART-Large**: For searching medical labels in text.
- **MedSpaCy**: For identifying genes and extracting relevant information.

## Installation

To get started, you'll need to install the following dependencies. Make sure you have Python 3.7 or higher installed on your system.

1. Clone this repository:

    ```bash
    git clone https://github.com/Da-MaRo/HSPA4_NLP.git
    cd HSPA4_NLP
    ```

2. Install the required Python packages:

    ```bash
    pip install -r requirements.txt
    ```

   `requirements.txt` should include:

    ```
    beautifulsoup4==4.10.0
    nltk==3.7
    transformers==4.21.1
    medspacy==0.2.1
    requests==2.26.0
    pandas==1.3.3
    regex==2021.8.3

    ```

## Usage

1. **Scrape Abstracts:**

    To scrape abstracts related to HSPA4 from PubMed, run:

    ```bash
    python Pubmed_Scraper_HSPA4.py
    ```

    This script will save the abstracts to a file named `pubmed_scraped_data_HSPA4.csv`.

2. **Process and Analyze Abstracts:**

    To preprocess the text data using NLTK, extract medical labels using BART-Large, and identify genes using MedSpaCy, run:

    ```bash
    python Pubmed_NLP_HSPA4.py
    ```

    This script will perform the following steps:
    - Preprocess the scraped abstracts and 
    - Identify and save medical labels to `zero_shot_classification_results.csv`
    - Extract genes and related information, saving the results to `important_entities_hspa4.csv`.

## Data Processing Workflow

1. **Web Scraping**:
   - Use Beautiful Soup to scrape abstracts from PubMed.
   - Store the abstracts in a CSV file.

2. **Text Preprocessing**:
   - Tokenize and clean text using NLTK.
   - Save the preprocessed data for further analysis.

3. **Medical Label Analysis**:
   - Utilize BART-Large to detect medical labels related to protein quality control.
   - Extract and save these labels.

4. **Gene Identification**:
   - Apply MedSpaCy to identify genes mentioned in the abstracts.
   - Analyze and save the gene-related data.

## Analysis and Results

The analysis involves:

- Extracting impactful sequences from the abstracts.
- Mapping these sequences to medical labels and genes related to HSPA4 and protein quality control.
- Providing insights and visualizations to highlight significant findings.

Results are available in the following files:

- `pubmed_scraped_data_hspa4.csv`
- `zero_shot_classification_results.csv`

## Contributing

Contributions to improve this project are welcome! If you have suggestions or want to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes and commit (`git commit -am 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

Feel free to explore the repository and make use of the provided scripts to analyze and understand HSPA4-related research. If you have any questions or run into issues, please open an issue or contact me.

Happy coding!
