# Named-Entity-Recognition-NER-in-NLP

This project focuses on developing a robust Named Entity Recognition (NER) pipeline tailored for noisy, unstructured Twitter data. Traditional hashtag-based content discovery methods are insufficient, hence this NER system enhances entity-level understanding to improve content tagging, trend analysis, and real-time insights.

🧾 Dataset Summary

Source: Pre-labeled Twitter NER dataset in CoNLL format.

Entities Covered: 10 fine-grained types – Person, Geo-location, Company, Facility, Product, Music Artist, Movie, Sports Team, TV Show, Other.

Format: BIO tagging scheme with one word and its corresponding label per line.

🔍 Exploratory Data Analysis (EDA)

Examined entity distribution using bar plots.

Identified imbalance: The majority of tokens labeled as “O” (non-entity).

Cleaned and structured entity-tagged sequences for modeling.

⚙️ Preprocessing

Converted data into sequences of tokens and tags.

Applied tokenization, padding, and encoding for model input.

Created embedding matrix using GloVe Twitter-200 pre-trained vectors.

Handled long/short tweet sequences uniformly using padding.

🤖 Models Implemented

BiLSTM + CRF Model

Leveraged bidirectional LSTM layers with a CRF layer for sequence labeling.

Trained on padded token sequences using one-hot encoded tag vectors.

Achieved ~96.1% accuracy on test set.

Transformer-Based Model (BERT)

Fine-tuned bert-base-uncased for token classification.

Utilized WordPiece tokenization with alignment to BIO tags.

Attained ~99.1% validation accuracy in 10 epochs.

📊 Evaluation Metrics

Used F1 Score, Precision, and Recall.

Compared entity-level accuracy for both CRF and BERT models.

Conducted prediction comparisons between models for multiple tweet samples.

✅ Key Takeaways

Transformer-based models outperform BiLSTM+CRF, especially in capturing complex entities.

Proper preprocessing and label alignment is critical for BERT NER accuracy.

Visualization helped understand annotation quality and class distribution.

