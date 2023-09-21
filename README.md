I'm a 3rd-year PhD student advised by [Prof. Michael Cafarella](https://scholar.google.com/citations?user=r1quzEkAAAAJ&hl=en) in the [Data Systems Group](http://dsg.csail.mit.edu/) at MIT CSAIL. I previously worked with [Prof. Rachel Pottinger](https://www.cs.ubc.ca/~rap/) and [Prof. Raymond Ng](https://www.cs.ubc.ca/~rng/) in the [Data Management and Mining Lab](https://www.cs.ubc.ca/labs/db/research.php) at the University of British Columbia.

Today, with the explosion of data, more and more people are in desperate need to access and make use of data in more and more fields, such as social science and healthcare. However, both domain-specific and programming skills are required for an individual to do so, but not everyone has the background. Inspired by such use cases, my current research focuses on developing methods to help users interact with and make sense of data using machine learning and programming language techniques. 

## On-Going Projects

### Automatic Standardization for Data Preprocessing
Data preparation is the process of cleaning, transforming, and structuring raw data into a format that is usable for downstream data-powered applications. Many data pipelines require a custom data preprocessing program. Although these programs embody technical and domain insights, they are difficult for others to understand and reuse because they are pipeline-specific and are written in general-purpose languages. As a result, these programs can easily become a breeding ground for poor engineering and statistical practices. Ideally, preprocessing scripts would be as standardized as possible among applications of a database, with a minimal portion tailored to the particular data application.  

We propose a novel script-standardization system, in which users start with a traditional application-specific draft of a preprocessing script. The system finds a standardized version of the user script that is "admirably boring" -- one with a fraction that is more common --- and thus more widely-tested and more easily-understood --- while preserving the user intent in the original script. We present an algorithmic framework that yields such scripts and implemented a prototype system, LucidScript. We evaluate our approach against several state-of-the-art methods, including GPT-4, on six real-world datasets, showing the effectiveness and robustness of our approach by improving script standardization up to 42% w.r.t. the user intent.

## Publications
[Workload-Aware Query Recommendation Using Deep Learning](https://openproceedings.org/2023/conf/edbt/paper-173.pdf) To Appear in IEEE EDBT '23.  
*<strong>Eugenie Y Lai</strong>, Zainab Zolaktaf, Mostafa Milani, Omar AlOmeir, Jianhao Cao, Rachel Pottinger*

[Summarizing Provenance of Aggregation Query Results in Relational Databases](https://ieeexplore.ieee.org/abstract/document/9458813) IEEE ICDE '21: 1955-1960. 
*Omar AlOmeir, <strong>Eugenie Lai</strong>, Mostafa Milani, and Rachel Pottinger*.

[Pastwatch: On the Usability of Provenance Data in Relational Databases](https://ieeexplore.ieee.org/abstract/document/9101356) IEEE ICDE '20: 1882-1885.  
*Omar AlOmeir, <strong>Eugenie Lai</strong>, Mostafa Milani, and Rachel Pottinger*.

## Other

<span style="font-size:18px;">[Blog](./blog.html)</span> for fun.

<span style="font-size:18px;">[Miscellaneous](./miscellaneous.html)</span> to de-stress.

