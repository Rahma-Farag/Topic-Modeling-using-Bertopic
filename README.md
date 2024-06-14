# Topic-Modeling-using-Bertopic
Topic modeling is a form of unsupervised ML using NLP modeling. It uncovers hidden themes or topics within a documnet. BERTopic is a topic modeling technique that leverages transformers and c-TF-IDF to create dense clusters allowing for easily interpretable topics whilst keeping important words in the topic descriptions.

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
    
    style B fill:#f9f,stroke:#333,stroke-width:4px;
    style D fill:#ff9,stroke:#333,stroke-width:4px;
    style F fill:#9f9,stroke:#333,stroke-width:4px;
    style H fill:#9ff,stroke:#333,stroke-width:4px;
    style J fill:#f99,stroke:#333,stroke-width:4px;
