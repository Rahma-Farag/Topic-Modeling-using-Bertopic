# Topic-Modeling-using-Bertopic
Topic modeling is a form of unsupervised machine learning (ML) using natural language processing (NLP) modeling. It uncovers hidden themes or topics within a collection of text documents called corpus. 

BERTopic is a topic modeling technique that leverages transformers and c-TF-IDF to create dense clusters allowing for easily interpretable topics whilst keeping important words in the topic descriptions.

The BERTopic pipeline consists of several key components that work together to generate coherent topics from textual data.

1. **Embedding Model**: Converts raw text documents into dense embeddings that capture the semantic meaning of the text.
2. **UMAP Model**: Reduces the high-dimensional embeddings into a lower-dimensional space to facilitate efficient clustering.
3. **HDBSCAN Model**: Clusters the reduced embeddings to identify groups of similar documents, representing different topics.
4. **Vectorizer Model**: Creates a sparse representation of the text (e.g., using TF-IDF) to help extract representative keywords for each topic.
5. **Representation Model**: Refines the topics by selecting the most relevant keywords or phrases from the sparse representation and clusters.

```mermaid
graph TD;
    A[Raw Text Documents] --> B[Embedding Model]
    B[Embedding Model] --> C[Dense Embeddings]
    C[Dense Embeddings] --> D[UMAP Model]
    D[UMAP Model] --> E[Lower-dimensional Embeddings]
    E[Lower-dimensional Embeddings] --> F[HDBSCAN Model]
    F[HDBSCAN Model] --> G[Clusters/Topics]
    A[Raw Text Documents] --> H[Vectorizer Model]
    H[Vectorizer Model] --> I[Sparse Matrix]
    G[Clusters/Topics] --> J[Representation Model]
    I[Sparse Matrix] --> J[Representation Model]
    J[Representation Model] --> K[Refined Topic Representations with Keywords]
    
    style B fill:#f9f,stroke:#333,stroke-width:2px;
    style D fill:#ff9,stroke:#333,stroke-width:2px;
    style F fill:#9f9,stroke:#333,stroke-width:2px;
    style H fill:#9ff,stroke:#333,stroke-width:2px;
    style J fill:#f99,stroke:#333,stroke-width:2px;
