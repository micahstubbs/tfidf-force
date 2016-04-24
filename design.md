force-directed layout of reuters articles

nodes: articles (article names)
links: entity (or token) co-occurence
link weights: sum of tf-idf values of co-occurring tokens (nouns?)
colors: k-means cluster groups using cosine similarity

(using tf-idf values as the spring forces)

hover over a node to preview contents (or put in a side panel for starters?)
article title visualized with the node (or on hover)

parse each article for filtered tokens of type noun with stop words and contractions removed

calculate tf-idf values using the reuters corpus as the corpus

for each pair of articles, if at least one word co-occurs, sum all co-occurring tf-idf values, add this as a link

run k-means, set the cluster number as the group number of the document

---

#### tasks

+ generate list of documents (articles)
+ generate list of entities
+ generate list of pairs of entities that co-occur (appear together)
+ calculate tf-idf values for all entities
+ calculate sum of tf-idf values for all pairs of co-occurent entities
+ generate graph data structure 