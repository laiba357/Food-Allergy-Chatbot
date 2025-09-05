# Food Allergy Chatbot

An AI-powered chatbot designed to help users manage food allergies by providing quick, accurate, and reliable information regarding emergency symptoms, precautions, treatments, and allergen-specific food data.

## Overview

Food allergies can pose severe health risks, and immediate access to reliable information is critical for effective management. This project utilizes Natural Language Processing (NLP) and a structured SQLite database to deliver essential food allergy-related information through an intelligent chatbot interface.

## Features

* **Comprehensive Dataset Integration**
  Includes CSV, PDF, and text sources, normalized into a structured SQLite database.

* **Interactive Chatbot**
  Answers user queries about food allergens, symptoms, and management.

* **Emergency Guidance**
  Provides immediate response information for critical allergy cases.

* **Modular Architecture**

  * Dataset Preprocessing (`table-creation.ipynb`)
  * Chatbot Development (`chatbot-development.ipynb`)

## Project Structure

```
Food_Allergy_Chatbot/
│── Complete Dataset/             
│   ├── Raw/                      
│   └── README_DATASET.md         
│── data/
│   └── food_allergy.db           
│── table-creation.ipynb          
│── chatbot-development.ipynb     
│── requirements.txt              
│── LICENSE                       
│── CITATION.cff                  
│── README.md                     
```

## Dataset

The dataset consolidates various food allergy-related resources:

* **CSV Files**: Allergy alerts and food data.
* **PDF Documents**: Educational and statistical reports.
* **Text Files**: Practical guidelines and symptom management protocols.

This data is parsed, normalized, and stored in an SQLite database (`food_allergy.db`) for efficient querying.

## Workflow

1. **Data Preprocessing**

   * Extract and clean raw datasets.
   * Create database schema with tables:

     * Emergency Symptoms
     * Precautions
     * Prevention Tips
     * Treatments
     * Food Data
     * Food Allergies
     * Product Recalls

2. **Database Creation**

   * Executed using `table-creation.ipynb`.
   * Ensures data integrity and portability.

3. **Chatbot Development**

   * Implemented in `chatbot-development.ipynb`.
   * Uses NLP techniques for user query understanding.
   * Fetches relevant data from the SQLite database.

## Installation

1. Clone the repository:

   ```
   git clone https://github.com/yourusername/Food_Allergy_Chatbot.git
   cd Food_Allergy_Chatbot
   ```

2. Install required dependencies:

   ```
   pip install -r requirements.txt
   ```

   Ensure you have Jupyter Notebook installed to run the `.ipynb` files:

   ```
   pip install notebook
   ```

## Usage

1. **Create the Database**
   Open and run `table-creation.ipynb`.

2. **Run the Chatbot**
   Open `chatbot-development.ipynb` and execute all cells.
   Interact with the chatbot by typing queries related to food allergies.

## Future Work

* Develop a user-friendly interface using Streamlit or Flask for real-time interaction.
* Expand the dataset to include global allergens and localized dietary data.
* Implement multi-language support for broader accessibility.
* Integrate with healthcare systems and electronic health records (EHR) for seamless clinical use.
* Deploy as a web application, API, or chatbot on popular platforms (Telegram, WhatsApp, etc.).

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Author

Developed by **Laiba Fatima**
