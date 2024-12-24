# YouTube Transcript Summarizer

This Python script extracts, processes, and summarizes the transcript of a YouTube video using natural language processing (NLP) techniques. The summarized text is generated for enhancing content consumption and knowledge acquisition.

## Features

- Extracts YouTube video transcripts using the `youtube-transcript-api`.
- Cleans and prerocesses the transcript text.
- Uses SpaCy for NLP tasks such as tokenization and stopword removal.
- Summarizes text using word frequency and BART Transformer model.
- Evaluates the summary using ROUGE and Flesch Reading Ease scores.

## Prerequisites

Before running the script, install:

- Python 3.7 or higher
- Jupyter Notebook
- Required Python libraries:
  - `spacy`
  - `transformers`
  - `youtube-transcript-api`
  - `wordninja`
  - `rouge-score`
  - `textstat`

The dependencies can be installed using pip:
```bash
pip install spacy 
pip install transformers 
pip install youtube-transcript-api 
pip install wordninja 
pip install rouge-score
pip install textstat
```

Additionally, download SpaCy's English language model:
```bash
python -m spacy download en_core_web_sm
```

## Usage

1. Download the repository containing this script.
2. Run the script in a Jupyter Notebook environment.

### Steps in the Script

1. **Import Libraries**
   - Required libraries are imported for processing, summarizing, and evaluating the text.

2. **Fetch Transcript**
   - Enter a YouTube video link when prompted.
   - The video ID is extracted, and its transcript is fetched using `youtube-transcript-api`.

3. **Process Text**
   - The transcript text is cleaned and split into meaningful tokens using `wordninja` and SpaCy.
   - Stopwords and punctuation are removed.

4. **Calculate Word Frequencies**
   - Frequencies of significant words are calculated and normalized.

5. **Sentence Scoring and Summarization**
   - Sentences are scored based on word frequencies.
   - The most important sentences (50% of the total) are selected.

6. **Generate Summary**
   - The BART model is used for text summarization in chunks.

7. **Evaluation**
   - The quality of the summary is evaluated using ROUGE metrics.
   - Readability is measured using the Flesch Reading Ease score.

### Running the Script

Run the script and follow these prompts:

- Paste the YouTube video link when asked.
- The final summary and evaluation scores will be printed at the end.

## Output

- **Summary**: A concise version of the YouTube video transcript.
- **Evaluation**:
  - ROUGE metrics: Measures the overlap between the original and summarized text.
  - Flesch Reading Ease Score: Indicates how easy the summary is to read.

## Limitations

- Requires videos with transcripts enabled.
- Summary quality depends on the accuracy of the transcript.

## References

- https://spacy.io/usage
- https://huggingface.co/docs/transformers/en/index
- https://pypi.org/project/youtube-data-api/
- https://pypi.org/project/wordninja/
- https://www.youtube.com/watch?v=6C0sLtw5ctc
- https://www.youtube.com/watch?v=9PoKellNrBc
- https://www.youtube.com/watch?v=LbX4X71-TFI&t=90s
- https://www.youtube.com/watch?v=QEaBAZQCtwE

## Author

Soham Singh Chouhan
