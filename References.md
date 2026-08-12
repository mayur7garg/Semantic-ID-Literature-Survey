# References
> All research papers, blogs and articles referenced or read for this survey

1. [Recommender Systems with Generative Retrieval](https://arxiv.org/pdf/2305.05065)
    - **Year**: 2023
    - **Type**: Research paper
    - **Topics covered**:
        - Transformer Index for GEnerative Recommenders (TIGER)
    - **Notes**:
        - Uses RQ-VAE

2. [Text Is All You Need: Learning Language Representations for Sequential Recommendation](https://arxiv.org/pdf/2305.13731)
    - **Year**: 2023
    - **Type**: Research paper

3. [IDGenRec: LLM-RecSys Alignment with Textual ID Learning](https://arxiv.org/pdf/2403.19021)
    - **Year**: 2024
    - **Type**: Research paper

4. [Learnable Item Tokenization for Generative Recommendation](https://arxiv.org/pdf/2405.07314)
    - **Year**: 2024
    - **Type**: Research paper
    - **Topics covered**:
        - LETTER (LEarnable Tokenizer for generaTivE Recommendation)
    - **Notes**:
        - Integrates hierarchical semantics, collaborative signals, and code assignment diversity
        - Uses a well-trained collaborative filtering model to align semantic quantized embeddings in RQ-VAE with CF embeddings
        -  Collaborative regularization encourages items with similar collaborative interactions to exhibit similar code sequences
        - Code diversity loss pulls embeddings from the same cluster closer and push the embeddings of codes from different clusters away
        - Loss for training codebooks - sum of semantic loss (from RQ-VAE), CF loss and diversity loss
        - Loss for generation - Ranking-guided generation loss with an adjustable temperature to penalize hard-negatives
    - **Datasets**:
        - Amazon review datasets (Instruments and Beauty)
        - Yelp
    - **Related works**:
        - TIGER

5. [Semantic IDs for Recommendation Systems: A Technical Deep Dive](https://januverma.substack.com/p/semantic-ids-for-recommendation-systems)
    - **Year**: 2025
    - **Type**: Blog

6. [Transformer Memory as a Differentiable Search Index](https://arxiv.org/pdf/2202.06991)
    - **Year**: 2022
    - **Type**: Research paper

7. [Learning Vector-Quantized Item Representation for Transferable Sequential Recommenders](https://arxiv.org/pdf/2210.12316)
    - **Year**: 2022
    - **Type**: Research paper

8. [Generative Recommendation with Semantic IDs: A Practitioner's Handbook](https://arxiv.org/pdf/2507.22224)
    - **Year**: 2025
    - **Type**: Research paper
    - **Topics covered**:
        - Generative Recommendation with semantic ID (GRID)
    - **Notes**:
        - Introduces an open-source framework GRID for prototyping generative recommendation with semantic IDs

9. [Better Generalization with Semantic IDs: A Case Study in Ranking for Recommendations](https://arxiv.org/pdf/2306.08121)
    - **Year**: 2023
    - **Type**: Research paper

10. [Differentiable Semantic ID for Generative Recommendation](https://arxiv.org/pdf/2601.19711)
    - **Year**: 2026
    - **Type**: Research paper
    - **Topics covered**:
        - DIGER (Differentiable Semantic ID for GEnerative Recommendation)
        - Differentiable SID framework with exploratory learning (DRIL) with Gumbel noise
    - **Notes**:
        - Most SIDs are optimized for content reconstruction instead of recommendation such as RQ-VAE
        - Since semantic IDs are precomputed and frozen, the recommendation loss cannot propagate gradients back.
        - Solution is to make IDs differentiable similar to MoRec. Issue is the discrete nature.
        - Most common workaround - straight-through estimator (STE) - can trigger SID collapse causing a small subset of codes to dominate.
        - Designed a differentiable SID framework with exploratory learning (DRIL) with Gumbel noise to address the codebook collapse.
        -  DIGER employs Soft Update, allowing gradients to flow to all codebook weighted by their Gumbel-Softmax probabilities, while the noise level is progressively reduced via uncertainty decay strategies (exploration -> exploitation).
        - Hard SID are used for forward indexing whereas gradients are updated using soft probabilities
    - **Datasets**:
        - B-Shop
        - I-Shop
        - Yelp
    - **Related works**:
        - TIGER
        - LETTER
        - ETEGRec

11. [Semantic-Enhanced Differentiable Search Index Inspired by Learning Strategies](https://arxiv.org/pdf/2305.15115)
    - **Year**: 2023
    - **Type**: Research paper

12. [TokenRec: Learning to Tokenize ID for LLM-based Generative Recommendation](https://arxiv.org/pdf/2406.10450)
    - **Year**: 2024
    - **Type**: Research paper

13. [Semantic IDs: Generative Retriever (Part-IV)](https://medium.com/better-ml/semantic-ids-generative-retriever-part-iv-ae7c34223fbc)
    - **Year**: 2025
    - **Type**: Blog

14. [OneRec: Unifying Retrieve and Rank with Generative Recommender and Iterative Preference Alignment](https://arxiv.org/pdf/2502.18965)
    - **Year**: 2025
    - **Type**: Research paper

15. [Semantic IDs for Joint Generative Search and Recommendation](https://dl.acm.org/doi/10.1145/3705328.3759300)
    - **Year**: 2025
    - **Type**: Research paper

16. [Understanding Generative Recommendation with Semantic IDs from a Model-scaling View](https://arxiv.org/pdf/2509.25522)
    - **Year**: 2025
    - **Type**: Research paper

17. [Training an LLM-RecSys Hybrid for Steerable Recs with Semantic IDs](https://eugeneyan.com/writing/semantic-ids/)
    - **Year**: 2025
    - **Type**: Blog

18. [YouTube gets ~5% CTR lift on Shorts by replacing embedding tables with Semantic IDs](https://www.shaped.ai/blog/youtube-semantic-ids-ctr-lift)
    - **Year**: 2025
    - **Type**: Blog

19. [Semantic IDs for Recommender Systems at Snapchat: Use Cases, Technical Challenges, and Design Choices](https://arxiv.org/pdf/2604.03949)
    - **Year**: 2026
    - **Type**: Research paper

20. [A Modular Survey for Semantic ID-Based Generative Recommendation](https://www.preprints.org/manuscript/202605.0619)
    - **Year**: 2026
    - **Type**: Research paper

21. [PLUM: Adapting Pre-trained Language Models for Industrial-scale Generative Recommendations](https://arxiv.org/pdf/2510.07784)
    - **Year**: 2025
    - **Type**: Research paper

22. [Deploying Semantic ID-based Generative Retrieval for Large-Scale Podcast Discovery at Spotify](https://arxiv.org/pdf/2603.17540)
    - **Year**: 2026
    - **Type**: Research paper

23. [Generating Long Semantic IDs in Parallel for Recommendation](https://arxiv.org/pdf/2506.05781)
    - **Year**: 2025
    - **Type**: Research paper

24. [End-to-End Semantic ID Generation for Generative Advertisement Recommendation](https://arxiv.org/pdf/2602.10445)
    - **Year**: 2026
    - **Type**: Research paper

25. [Unleash the Potential of Long Semantic IDs for Generative Recommendation](https://arxiv.org/pdf/2602.13573)
    - **Year**: 2026
    - **Type**: Research paper

26. [Purely Semantic Indexing for LLM-based Generative Recommendation and Retrieval](https://arxiv.org/pdf/2509.16446)
    - **Year**: 2025
    - **Type**: Research paper

27. [FORGE: Forming Semantic Identifiers for Generative Retrieval in Industrial Datasets](https://arxiv.org/pdf/2509.20904)
    - **Year**: 2025
    - **Type**: Research paper

28. [Mitigating Collaborative Semantic ID Staleness in Generative Retrieval](https://arxiv.org/pdf/2604.13273)
    - **Year**: 2025
    - **Type**: Research paper

29. [The Foundations of Generative Recommendation with Semantic ID — Chapter 3 (Algorithm)](https://medium.com/@harshnpathak/the-foundations-of-generative-recommendation-with-semantic-id-chapter-3-algorithm-ee0acb43f52d)
    - **Year**: 2025
    - **Type**: Blog

30. [Generative Recommender with End-to-End Learnable Item Tokenization](https://arxiv.org/pdf/2409.05546)
    - **Year**: 2024
    - **Type**: Research paper
    - **Topics covered**:
        - ETEGRec (End-To-End Generative Recommender)
        - Provides a good summary of existing methods of generating SIDs including parameter-free and clustering methods.
    - **Notes**:
        - Current approaches have item tokenization and generative recommendation training as separate processes.
        - Introduces two key optimization objectives: sequence-item alignment and preference-semantic alignment.
        - Developed an alternating optimization technique.
        - Uses 4 losses - Reconstruction loss, recommendation loss and two alignment loss in an alternating optimization scheme to train the model.
        - Is interaction aware like GPTRec
    - **Datasets**:
        - 3 subsets of the most recent Amazon 2023 review data -  Musical Instruments, Video Games, and Industrial Scientific
    - **Related works**:
        - TIGER
        - LETTER