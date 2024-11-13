# Combining Lexical and Semantic Retrievals for Query Search using LLMs
This project explores the integration of lexical and semantic retrieval methods to improve query search accuracy. Traditional search engines typically rely on either lexical or semantic-based approaches. Our work combines both methods to leverage the strengths of each, leading to improved overall retrieval accuracy and contextual relevance.

## Problem Statement
Traditional search engines typically rely on one of two types of retrieval methods:

Lexical retrieval (e.g., BM25) that matches keywords in the query with documents.
Semantic retrieval that aims to understand the meaning or context behind the query.
While both approaches are effective, they have their limitations when used alone. By combining these methods, we aim to enhance retrieval performance by improving the quality and relevance of search results.

## Approach
This study integrates lexical (BM25) and semantic (DistilBERT) retrieval techniques to improve search accuracy. The key idea is to combine the traditional lexical search with a semantic understanding of the query, which together offer more accurate and contextually relevant search results.

## Methods Used
BM25: A traditional and highly effective lexical retrieval method.
DistilBERT: A lightweight version of BERT, which is used for semantic search and understanding contextual meanings behind queries.

## Datasets
We evaluated the performance of our integrated approach using two benchmark datasets:

### Scifact: A dataset focused on factual retrieval.
### Tiny MS Marco: A popular dataset for evaluating information retrieval models.

## Evaluation Metrics
nDCG (Normalized Discounted Cumulative Gain)
MAP (Mean Average Precision)
These metrics are used to measure the effectiveness of the retrieval system in returning relevant documents in response to a given query.

## Results
Our evaluation shows that ensemble methods that combine both lexical and semantic retrieval outperform individual approaches. Specifically, the combination of DistilBERT and BM25 achieved notable performance improvements across both datasets, even without the need for fine-tuning the models.

Significant improvements were observed in metrics like nDCG and MAP, showing the effectiveness of the ensemble approach.
The integration of lexical and semantic methods leads to more robust search results, with enhanced retrieval accuracy and contextual relevance.

## Key Findings
Ensemble methods outperform individual retrieval approaches.
The combination of BM25 (lexical) and DistilBERT (semantic) results in significant improvements in search accuracy.
No fine-tuning required: Even without fine-tuning the models, the integrated approach provided robust performance improvements.

## Conclusion
In this paper, we explored the potential of combining lexical and semantic retrieval techniques to enhance the performance of information retrieval systems. Our experiments, conducted on the Scifact and MS Marco Tiny datasets, demonstrate that ensemble methods integrating BM25 with advanced language models such as distilBERT and RepLlama significantly outperform their standalone counterparts.
The results show that ensemble approaches, particularly the combination of distilBERT_bm and BM25, consistently achieve higher nDCG@10, MAP@10, Recall@10, and P@10 scores compared to individual lexical and semantic methods. This indicates a balanced improvement in both precision and contextual understanding, addressing the limitations of traditional IR methods.
Notably, RepLlama, despite not being fine-tuned on the Scifact dataset, benefited from the ensemble approach, highlighting that even in zero-shot scenarios, where fine-tuning data and resources are unavailable, combining lexical and semantic methods can still enhance retrieval performance without additional fine-tuning.

Future work could explore further optimization of ensemble weights and the integration of additional retrieval techniques to continue improving search accuracy and efficiency. Additionally, extending this approach to other datasets and real-world scenarios could provide deeper insights into its applicability and robustness across different contexts.
