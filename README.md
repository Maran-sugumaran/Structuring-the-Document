# Structuring-the-Document
A document is represented as a collection paragraphs, a paragraph is represented as a collection of sentences, a sentence is represented as a collection of words and a word is represented as a collection of lower-case ([a-z]) and upper-case ([A-Z]) English characters. You will convert a raw text document into its component paragraphs, sentences and words. To test your results, queries will ask you to return a specific paragraph, sentence or word as described below.

Alicia is studying the C programming language at the University of Dunkirk and she represents the words, sentences, paragraphs, and documents using pointers:

A word is described by:
struct word {
    char* data;
};
A sentence is described by:
struct sentence {
    struct word* data;
    int word_count;//the number of words in a sentence
};
The words in the sentence are separated by one space (" "). The last word does not end with a space.

A paragraph is described by:
struct paragraph {
    struct sentence* data  ;
    int sentence_count;//the number of sentences in a paragraph
};
The sentences in the paragraph are separated by one period (".").

A document is described by:
struct document {
    struct paragraph* data;
    int paragraph_count;//the number of paragraphs in a document
};
The paragraphs in the document are separated by one newline("\n"). The last paragraph does not end with a newline.
