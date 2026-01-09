# Text-Summarization-Using-Transformer-Models

Built an automatic text summarization system using Transformer-based sequence-to-sequence models to generate concise and meaningful summaries from large text inputs. The project demonstrates the practical use of NLP and deep learning for content condensation and insight extraction.

## Objective
The objective of this project is to develop an NLP-based system that can automatically generate high-quality summaries from raw text reviews, helping users quickly understand key information from large volumes of text.

## Dataset Overview
- Input data consists of multiple text reviews stored in a text file (`reviews.txt`)
- Each line represents an individual review
- Text data is unstructured and varies in length

## Model & Tokenization
- Used a **pre-trained Transformer-based Seq2Seq model** for abstractive summarization
- Model: `Falconsai/text_summarization` (Hugging Face)
- Tokenization handled using the model’s corresponding tokenizer
- Input text is truncated to a maximum length to ensure efficient processing

## Text Preprocessing
- Removed empty lines from input file
- Prepended summarization instruction (`summarize:`) to each review
- Applied token truncation to handle long reviews

## Summarization Pipeline
- Encoded input text using the tokenizer
- Generated summaries using beam search for better output quality
- Controlled summary length using minimum and maximum length constraints
- Decoded generated tokens into human-readable summaries

## Model Configuration
- Beam search: `num_beams = 8`
- Length penalty applied to avoid overly long summaries
- Early stopping enabled for efficient generation
- Maximum input length limited to 512 tokens

## Output
- Original reviews printed alongside generated summaries
- Each review produces a concise abstractive summary
- Output is suitable for quick reading and analysis

## Use Cases
- Customer review summarization
- Feedback analysis
- Document condensation
- Content understanding and reporting
- NLP-driven business insights

## Business Insights
- Enables faster understanding of customer feedback
- Reduces manual effort in reading long reviews
- Helps businesses identify key themes and sentiments efficiently
- Improves decision-making through concise textual insights

## Limitations
- Performance depends on the quality of the pre-trained model
- Very long documents require chunking for optimal results
- Domain-specific language may require fine-tuning

## Future Enhancements
- Fine-tune the model on domain-specific review data
- Add batch processing for large-scale datasets
- Integrate sentiment analysis with summaries
- Build a web interface using Streamlit or Flask

## Technologies Used
- Python
- Hugging Face Transformers
- PyTorch
- NLP (Natural Language Processing)

## Skills Demonstrated
- Natural Language Processing
- Transformer Models
- Text Summarization
- Deep Learning
- Model Inference with Hugging Face
