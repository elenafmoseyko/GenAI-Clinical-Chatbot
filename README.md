# Development and Integration of a HER2 Q/A Chatbot Using Unified Clinical Vocabulary Embeddings for Precision Medicine

## Overview
This project describes the development of a Q/A chatbot prototype designed to answer queries related to the publication "Human Breast Cancer: Correlation of Relapse and Survival with Amplification of the HER-2/neu Oncogene." It integrates insights from the "Unified Clinical Vocabulary Embeddings for Advancing Precision Medicine" research to improve clinical relevance and response accuracy.

## Key Features
- Integration of precomputed clinical embeddings for semantic relevance.
- Utilization of cosine similarity thresholds to identify clinically meaningful relationships.
- Enhanced precision in responses to HER2-related breast cancer queries.

## Integration of Clinical Embeddings
The chatbot integrates unified clinical vocabulary embeddings by:
- Loading precomputed embeddings (`full_h_embed_hms.pkl`) and node mappings (`new_node_map_df.tab`).
- Applying cosine similarity thresholds (initially 0.7, optimized to 0.9) to ensure high relevance in clinical associations.
- Improving the chatbot's accuracy through clinically validated connections.

## Data Sources
The chatbot relies on validated and authoritative data sources:
- Primary content from "Human Breast Cancer: Correlation of Relapse and Survival with Amplification of the HER-2/neu Oncogene" (Slamon et al., 1987).
- Precomputed embeddings (`full_h_embed_hms.pkl`) capturing semantic relationships among medical concepts.
- Node mapping file (`new_node_map_df.tab`) linking clinical terminologies to their respective indices.

## Prototype Implementation
The chatbot was developed using Python, leveraging these libraries:
- **Transformers (Hugging Face)**: GPT-Neo-125M model for text generation.
- **Fitz (PyMuPDF)**: Extracting and processing PDF content.
- **Scikit-learn**: Cosine similarity computations.
- **Pickle**: Efficient loading and storage of embeddings.
- **Requests**: Automated retrieval of required files.
- **Regular Expressions (re)**: Text cleaning and formatting.
- **Pandas and NumPy**: Data manipulation and numerical operations.

## Evaluation Approach
Comprehensive evaluation included:
- Extraction and integration of PDF content and reference tables.
- Explicit prompts guiding concise and evidence-based responses.
- Post-processing to ensure clarity and remove redundancy.

### Key Performance Indicators (KPIs)
- **Response Accuracy**: Verified using metrics like BLEU, ROUGE, and manual expert reviews.
- **User Satisfaction**: Measured via surveys and feedback on chatbot utility.
- **Response Time**: Monitored to ensure real-time responsiveness and user-friendly interactions.

### Testing Methodology
Extensive testing using diverse queries validated chatbot performance, robustness, and response accuracy. Queries ranged from basic definitions to complex clinical scenarios, with iterative refinements ensuring high-quality outputs.

## Continuous Improvement Strategy
An ongoing feedback loop captures user insights and performance data, facilitating iterative refinements to enhance chatbot accuracy, relevance, and user experience.

## Assumptions for Development
- **Data Availability**: Assumed accuracy and accessibility of primary research and reference data.
- **User Base**: Designed for a diverse audience including clinicians, researchers, healthcare providers, and general users seeking HER2-related information.
- **Data Quality**: Input data and embeddings are assumed thoroughly cleaned and validated.
- **Embedding Quality and Thresholds**: Cosine similarity thresholds based on published research findings, adjusted empirically for this dataset.
- **Model Consistency**: Assumed consistency in embedding model behavior relative to published research benchmarks.

