# Gensim Similarity Queries

📝 **Description:**
demonstrates querying a corpus for similar documents using Gensim.

## Creating the Corpus
To begin, we need to create a corpus to work with. If you have already completed this step in a previous tutorial, feel free to skip to the next section.

## Similarity Interface
In the previous tutorials, we covered the creation of a corpus in the Vector Space Model and how to transform it between different vector spaces. The aim is to determine similarity between pairs of documents or the similarity between a specific document and a set of other documents.

To illustrate this using Gensim, we'll consider the same corpus as in the previous examples. We'll first define a 2-dimensional LSI space.

For more details on LSI, refer to [Latent Semantic Indexing](https://en.wikipedia.org/wiki/Latent_semantic_indexing).

## Initializing Query Structures
To prepare for similarity queries, we need to input all documents we want to compare against subsequent queries. 

**Warning:**
The `similarities.MatrixSimilarity` class is only suitable when the whole set of vectors fits into memory.

If the data exceeds memory limits, consider using the `similarities.Similarity` class, which operates in fixed memory by splitting the index across multiple files on disk.

Index persistency is handled via the standard `save` and `load` functions.

## Performing Queries
To obtain similarities of our query document against the indexed documents:

Note that documents such as "The EPS user interface management system" and "Relation of user perceived response time to error measurement" may not be returned by a standard boolean fulltext search, but after applying LSI, they receive high similarity scores, indicating semantic relatedness.

## Where Next?
Congratulations on completing the tutorials! For further details, you can browse the API reference, wiki, or explore distributed computing in Gensim.

Gensim is a mature package used successfully by many individuals and companies for rapid prototyping and production. However, there's always room for improvement:

- Efficiency enhancements
- Parallelism utilization
- Keeping up with new algorithms

Gensim's mission is to facilitate easy experimentation with popular topic modelling algorithms on large datasets and to aid in prototyping new algorithms.

--- 
