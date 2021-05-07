I'm a senior undergraduate student in the Combined Major of Business and Computer Science (BUCS) program at the University of British Columbia (UBC). I have been working with [Dr. Rachel Pottinger](https://www.cs.ubc.ca/~rap/) since Spring 2019 and was previously advised by [Dr. Raymond Ng](https://www.cs.ubc.ca/~rng/).

My current research focuses on data systems while applying visualization and machine learning to help users interact with and make sense of data. Today, databases provide a vital infrastructure for users to access high volumes of data, but both field-specific and database-related expertise are required for a user to interact with database applications. Such use cases motivate my work on facilitating user interaction with data systems.

## Projects

### Sequence-Aware Query Recommendation Using Deep Learning

Users interact with database management systems by writing sequences of queries. Those sequences encode important information. Current SQL query recommendation approaches do not take that sequence into consideration. Our work presents a novel sequence-aware approach to query recommendation. We use deep learning prediction models trained on query sequences extracted from large-scale query workloads to build our approach. We present users with contextual (query fragments) and structural (query templates) information that can aid them in formulating their next query. We thoroughly analyze query sequences in two real-world query workloads, the Sloan Digital Sky Survey (SDSS) and the SQLShare workload. Empirical results show that the sequence-aware, deep-learning approach outperforms methods that do not use sequence information. \[[Manuscript](/assets/manus/seq-aware_query_recommendation.pdf) submitted to VLDB '21\] \[[Poster](/assets/posters/NCRC_poster.pdf)\]

### PastWatch

Pastwatch helps users understand query answers by summarizing, explaining, and visualizing query provenance. Data provenance is any information about the origin of data and the process that leads to its creation. The provenance of a query over a database is a subset of the data in the database that contributed to the query answer. While comprehensive, query provenance consists of large volumes of data and hence is overwhelming for users to explore. We present an approach to provenance exploration that builds on data summarization techniques and provides an interface to visualize the summary.

## Publications

Summarizing Provenance of Aggregation Query Results in Relational Databases \[[Short Paper](https://www.cs.ubc.ca/~mkmilani/report.pdf)\]. To Appear in IEEE ICDE '21.  
*Omar AlOmeir, <strong>Eugenie Y. Lai</strong>, Mostafa Milani, and Rachel Pottinger*.

Pastwatch: On the Usability of Provenance Data in Relational Databases \[[Short Paper](https://www.cs.ubc.ca/~mkmilani/pastwatch.pdf)\]. IEEE ICDE '20: 1882-1885.  
*Omar AlOmeir, <strong>Eugenie Y. Lai</strong>, Mostafa Milani, and Rachel Pottinger*.

## Other

<span style="font-size:18px;">[Blog](./blog.html)</span> for fun.

<span style="font-size:18px;">[Miscellaneous](./miscellaneous.html)</span> to de-stress.

