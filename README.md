
This was a project in the second semester of my masters, in which a selection of the learned technologies were combined. The goal was to test the combination of a graph- and a vector database to a combined RAG-System in order to compare book and series adaptions in the example of Pretty Little Liars. The agent runs locally using ollama. A detailed explanation of the technology and analysis of results can be found in [Capstone_Report.pdf](./Capstone_Report.pdf)

```
## Structure

Series                                      # Folder that contains everything for the two retrieval systems for the episode 
|-- Series.dump                             # Contains the dump of the neo4j database for the series entity-relationship-graph
|-- entities.json                           # contains the raw, extracted entities for graph database
|-- relationships.json                      # contains the raw-extracted for graph database
|-- entities_cleaned.json                   # contains the final entities for graph database
|-- relationships_cleaned.json              # contains the final entities for graph database
|-- PrettyLittleLiars_Episodes.csv          # contains all of the summaries of the episodes
|-- DataCollection_Series.ipynb             # This is the full data engineering code that scrapes the web, extracts entities and relationships, puts them into a graph database and puts the text chunks into a vector database

Books                                       # Folder that contains everything for the two retrieval systems for the book summaries
|-- Books.dump                              # Contains the dump of the neo4j database for the books entity-relationship-graph
|-- entities.json                           # contains the raw, extracted entities for graph database
|-- relationships.json                      # contains the raw-extracted for graph database
|-- entities_cleaned.json                   # contains the final entities for graph database
|-- relationships_cleaned.json              # contains the final entities for graph database
|-- PrettyLittleLiars_Books.csv             # contains all of the summaries of the books
|-- DataCollection_Books.ipynb             # This is the full data engineering code that scrapes the web, extracts entities and relationships, puts them into a graph database and puts the text chunks into a vector database

Chroma_db                                   # Contains vector database
Graph_rag.ipynb                             # The actual GraphRAG system that retrieves the context from the databases and generates an answer to the input question
```
