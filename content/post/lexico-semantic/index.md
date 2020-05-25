---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Identification Of Lexico-semantic Word Relations - A Beginner's Guide"
subtitle: ""
summary: ""
authors: ["Karan Praharaj"]
tags: ["Deep Learning", "Natural Language Processing", "Word Similarity"]
categories: []
date: 2020-02-22T19:07:15+05:30
lastmod: 2020-02-22T19:07:15+05:30
featured: true
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

When I tell you "this teddy bear is fluffy", 

Understanding human language is a difficult problem for computers. Unlike you and me, computers do not have the privilege of human language training the way we do. Even programming languages aren't directly interpreted by them - they are first converted to low-level machine language. True *machine code* is a stream of raw, usually binary (1s and 0s), data. 

While humans acquire the ability to parse, process, infer and communicate -- all of which we are doing right now, by way of this essay -- for the computer, any word picked out from a human language is unintelligible gibberish until it is adequately trained to understand the language.

This task of teaching and empowering machines to understand language just as we do, is called Natural Language Processing or NLP. NLP is a branch of artificial intelligence and it is an umbrella itself for many other subproblems. Daily examples of such problems are search, speech recognition, translation, summarization, question-answering etc. But all of this begs the question - if computers can understand nothing but 1s and 0s, how can computers make sense of the complexities of human language? 

Consider a space where all words in the English language are populated based on their semantic character. This imaginary space is such that words sharing similar share similar spacial properties. For instance, the words "cat" and "dog" would be in close vicinity with each other because the idea of a cat is very similar to the idea of a dog. Both are bipedal, domestic species that make for cute pets. For words that are not similar in meaning but represent the same concept, the positions of the words relative to each other encapsulate the relationship. In the semantic space, the relative position of "king" to the position of "queen" would be similar to the difference in relative positions between "man" and "woman" or "boy" and "girl", because the defining concept that separates the words is the same -- gender. 

Since words in their purest form cannot be interpreted by computers, we dumb them down by mapping the concepts and ideas that are inherent to the words into a representative set of numbers for each word. These sets of numbers are generated or "learned" algebraically by "neural networks" (a type of algorithm) and are called "word vectors". These word vectors bear the ability to capture information about semantic relationships and syntactic structures across collections of words. Approaches to generating word vectors build on Firth's (1957) *distributional hypothesis* which states:

> "You shall know a word by the company it keeps."

Put differently, **words that share similar contexts tend to have similar meanings**.

We will not delve into the mathematical details of how neural networks learn word embeddings, but now you know the underlying idea that drives the mathematics. 

My current research work is focused on a problem called lexical relation resolution. A lexical relation is a culturally recognized pattern of association that exists between lexical items (a word, a part of a word, or a chain of words) in a language. For example, the lexical relation between "open" and "close" is that of antonymy, whereas "close" and "shut" are connected by a synonymy relationship. Other asymmetric lexico-semantic relations include co-hyponymy (e.g. phone &larr;&rarr; monitor), hypernymy (e.g. phone &rarr; speakerphone) or meronymy (e.g. phone &rarr; mouthpiece), etc

Recognizing the exact nature of the semantic relation holding between a given pair of words is crucial and forms the basis for all the other NLP applications (question-answering, summarization, speech recognition etc.) that I mentioned above. 

Several methods have been proposed in the past to discriminate between multiple semantic relations that hold between a pair of words. But, this continues to remain a difficult task, especially when it comes to distinguishing between certain relations. (e.g synonymy and hyperonymy).

To solve this problem, our work proposes to investigate the introduction of related words in the neighbourhood of a particular word and gauge the effect it has on the prediction accuracy of word relations. Our original hypothesis was that if each word is augmented by the word vectors of a fixed number of neighbouring words (or "patches"), improved performance might be attained. 

However, our initial findings showed that the direct introduction of neighbour words did not lead to improvements. We figured that this was mainly due to a loss of concept-centrality that took place as a result of the change in strategy. If word relations are to be assessed by juxtapositioning two patches instead of two words, the required focus on the original word may be diluted.

The next logical step was to somehow weigh the word vectors based on their centrality to the concept. To do this, we introduced an **attention mechanism** based on the PageRank algorithm (which is one of the algorithms used by Google for their web search. PageRank was developed to measure the importance of website pages). We use it to assign a weight of centrality to each of the word neighbours in the patch. The more a word is central in the patch, the higher the score it receives. These scores are then to be used as attention weights to the corresponding word vector representations of the neighbours. The objective of this mechanism is to improve the predictive ability of our system based on the importance score of each word embedding in the patch. We found that when deployed in combination with the correct architecture, attention-adjusted patches gave a significant boost to previous results.











