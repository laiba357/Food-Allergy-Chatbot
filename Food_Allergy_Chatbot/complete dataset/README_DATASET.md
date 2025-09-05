# Food Allergy Chatbot

## Overview
This project presents the development of an **AI-powered chatbot** for food allergy management. The chatbot leverages **transformer-based language models (DistilBERT)** to help users identify potential allergens, receive emergency guidance, and access educational resources.  

The system integrates a **manually collected dataset** from multiple sources (CSV, PDFs, text files), structured into a **SQLite database** for efficient querying. By fine-tuning an LLM on this domain-specific dataset, the chatbot delivers **accurate, personalized, and context-aware responses** to user queries.

## Features
- Curated dataset of food items, allergens, symptoms, treatments, and precautionary measures.
- SQLite database (`data/food_allergy.db`) designed for fast and reliable queries.
- Transformer-based chatbot model (DistilBERT) fine-tuned for allergy management.
- Preprocessing pipeline with tokenization, padding, and sequence formatting for NLP tasks.
- Evaluation with metrics such as **accuracy, precision, recall**.

## Project Structure
## Project Structure
Food_Allergy_Chatbot/ <br>
│── Complete Dataset/             # Raw dataset files and documentation <br>
│   └── Raw/                      # Unprocessed source files <br>
│   └── README_DATASET.md         # Dataset documentation <br>
│── data/ <br>
│   └── food_allergy.db           # Final structured dataset (SQLite) <br>
│── table-creation.ipynb          # Notebook for database table creation <br>
│── chatbot-development.ipynb     # Notebook for chatbot implementation <br>
│── requirements.txt              # Python dependencies <br>
│── LICENSE                       # MIT License for open-source distribution <br>
│── CITATION.cff                  # Citation metadata for academic/research use <br>
│── README.md                     # Main project documentation <br>


## Data Sources
The dataset was built from:
1. **CSV files** – food data, allergy alerts, product recalls.  
2. **PDF documents** – facts, statistics, emergency care guides (FARE).  
3. **Text files** – practical guidelines, symptom management, testing procedures.  

These were normalized, structured, and integrated into a relational schema in SQLite.

## Database Schema
The database contains multiple tables:
- `EmergencySymptoms` – symptoms and severity of allergic reactions.  
- `Precautions` – do’s and don’ts for allergy management.  
- `PreventionTips` – tips to avoid allergen exposure.  
- `AllergyTestDetails` – diagnostic test information.  
- `Treatments` – emergency and long-term treatment options.  
- `FoodData` – categorized food items and allergens.  
- `FoodAllergies` – mappings between foods and allergy types.  
- `ProductRecalls` – records of food recalls due to allergens.  

## Model
- **Base Model**: DistilBERT (`distilbert-base-uncased`)  
- **Task**: Sequence classification for allergy-related queries.  
- **Training**:
  - Optimizer: AdamW  
  - Epochs: 10  
  - Learning rate scheduling with warm-up  
  - Evaluation split: 80% training / 20% validation  

## Results
The chatbot demonstrated:
- High accuracy in classifying allergy-related queries.  
- Strong precision and recall in identifying relevant allergen information.  
- Ability to provide contextually appropriate emergency advice.  

## Future Work
- Develop a user interface (Streamlit/Flask) for interactive use.  
- Expand dataset coverage to include more allergens and regions.  
- Integrate with healthcare systems and EHR platforms.  
- Deploy as a web app or API for real-world use.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Citation
If you use this project in research, please cite it using the [CITATION.cff](CITATION.cff).