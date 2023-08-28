
# Retrieval and Reranking

Retrieval and reranking are two complementary techniques often used in information retrieval systems to enhance the accuracy and relevance of search results.


## Retrieval and Rerank pipeline
![Pipeline](data:image/png;base64,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)

The retrieval and reranking pipeline is a two-step process used in information retrieval systems to efficiently provide users with relevant search results.

In the retrieval step, an initial set of potentially relevant documents is identified based on queries or search terms. This step involves techniques like vector similarity using models such as BiEncoders.

Reranking takes the initial set of retrieved documents and applies more sophisticated models and features to reorder them. 

This step aims to improve the precision and relevance of search results by considering finer aspects of semantic understanding, user behavior, and preferences. 

## Biencoders
![biencoder](data:image/png;base64,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)

BiEncoders are neural network architectures used in the retrieval process of information retrieval systems.
#### Query encoding:
   The query encoder takes a user's query or search term as input and transforms it into a fixed-dimensional vector representation.
#### Document Encoding:
   The document encoder performs a similar process but on the documents or text snippets in the database. 
#### Scoring and Ranking:
Once queries and documents are encoded, the similarity between a query and each document is computed.
This is typically done using vector similarity measures such as dot product or cosine similarity.
#### Retrieval:
 The documents with the highest scores are considered more relevant and are presented to the user as the search results.

 ## Crossencoders:
 ![crossencoder architecture](data:image/png;base64,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)
 CrossEncoders are neural network architectures used in the retrieval process of information retrieval systems. 
 #### Joint Encoding:
 CrossEncoders take pairs of queries and documents as input. These pairs are concatenated or combined in some way to form a joint representation that captures the interactions between the query and the document.

#### Encoding Interaction:
The joint representation is passed through the CrossEncoder architecture, which is designed to capture the combined semantics of the query and the document.
#### Scoring and Ranking:
Similar to BiEncoders, the CrossEncoder computes a similarity score between the joint-encoded query-document pair.
#### Retrieval:
Documents are ranked based on their similarity scores to the query. The documents with the highest scores are considered more relevant and are presented to the user as the search results.

