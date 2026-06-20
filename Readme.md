# NLP for Machine Learning

![images\image.png](images\image.png)

Example/UseCases = Auto Correct, In any messaging bots we get suggestions for the message reply. Language Translation, Text Classifications etc..

### Topics:

- **Corpus**: A large and structured collection of text (or speech) data used for language analysis and training models.
Example: All Wikipedia articles, A dataset of movie reviews
- **Documents**: A **document** is a single unit of text inside a corpus.
Example: If your corpus = 100 emails, Then each email = 1 document
- **Vocabulary**: A **vocabulary** is the set of all unique words in the corpus.
Example: Corpus: "I love NLP. NLP is fun." → Vocabulary: {I, love, NLP, is, fun}
- **Words (Tokens)**: Words (or **tokens**) are the basic units of text after processing.
Example: Sentence: "NLP is amazing!"  Tokens: ["NLP", "is", "amazing", "!"] These are the smallest pieces used for analysis.

# Tokenization:

**Tokenization** is the process of breaking text into smaller units called **tokens**.
Tokenization: converts text to into format machines can understand.

## Tokens:

Tokens are the basic building blocks of text. They can be:

- Words
- Sentences
- Characters
- Subwords

 Types of Tokenization:

- Word Tokenization: Splits text into words.
"Machine learning is fun" → ["Machine", "learning", "is", "fun"]
- Sentence Tokenization: Splits text into sentences.
"Hello world. NLP is cool.” → ["Hello world.", "NLP is cool."]
- Character Tokenization: Splits into individual characters.
"Hi” → ["H", "i"]
- Subword Tokenization (advanced): Used in modern NLP models (like BERT, GPT)
"unhappy" → ["un", "happy"]

## Stemming

It’s the process of reducing a word to its word stem that affixes to suffixes and prefixes or to the root of words known as a lemma. Stemming is important in natural language understanding (NLU) and natural language processing (NLP)

### Example

Original sentence:

> "The students are studying and studied hard for their studies."
> 

After stemming:

| Original Word | Stem |
| --- | --- |
| students | student |
| studying | studi |
| studied | studi |
| studies | studi |

Notice that the stem **"studi"** is not a valid English word. Stemming focuses on reducing words mechanically, not necessarily producing meaningful dictionary words.

### Popular Stemming Algorithms

1. **Porter Stemmer**
    - Most widely used.
    - Applies a series of suffix-removal rules.
2. **Snowball Stemmer**
    - Improved version of Porter Stemmer.
    - Supports multiple languages.
3. **Lancaster Stemmer**
    - More aggressive.
    - Produces shorter stems.

### Advantages

- Reduces vocabulary size.
- Improves search and document matching.
- Faster text processing.

### Disadvantages

- Can produce meaningless stems (e.g., *studi*).
- Different words may incorrectly map to the same stem.
- Less accurate than lemmatization for understanding meaning.

## Lemmatization

**Lemmatization** is an NLP technique that converts a word to its **lemma**, which is its dictionary or canonical form. Unlike stemming, lemmatization considers the word's meaning and grammatical context, so it usually produces valid words.

| Stemming | Lemmatization |
| --- | --- |
| Removes suffixes using rules | Uses vocabulary and grammar |
| Faster | Slower |
| May produce non-words | Produces valid dictionary words |
| Example: "studies" → "studi" | "studies" → "study" |

But it’s slower than the stemming technique, as it tries to get the root word from WordNet corpus.

- **Need speed and simpler matching? → Use Stemming**
- **Need accurate language understanding? → Use Lemmatization**

So, we use Lemmatization is chatbot, Q&A, Machine Translation etc.

and we use stemming in search engines, information retrieval, Document Indexing, spam detection/classification problems etc.

## Stop Words:

**Stopwords** are common words in a language that usually carry little semantic meaning by themselves and often appear very frequently in text. Examples in English include:
why needed?

- Reduced Data Size
- Improves Text Analysis
- Better search and information retrieval
- Improves feature extraction