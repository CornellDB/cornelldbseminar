# About

The Cornell Database Seminar covers recent research in the database area. The seminar meets weekly on Tuesdays from 3 to 4 PM ET. All talks by external speakers are **public** and can be attended via Zoom (link [here](https://cornell.zoom.us/j/94791289427?pwd=c2grd2dvc2xnWHpuLzMvemNub3BPZz09)). Talk recordings, without Q&A, will be available [online](https://www.youtube.com/playlist?list=PLXPbT_PYOiRhWH5G7GJdKKirILbO56Mmv). The seminar is organized by the [Cornell Database Group](https://itrummer.github.io/dbgrouphp/).

Talk details and recordings from Spring 2022 can be found [here](/cornelldbseminar/spring22.html).

# Schedule

|Date|Speaker|Talk|
|---|----- | ------- |
|8/23|Immanuel Trummer, _Cornell University_|Intro|
|8/30|(Internal)||
|9/6|(Internal)||
|9/13|Immanuel Trummer, _Cornell University_||
|9/20|Immanuel Trummer, _Cornell University_||
|9/27|Aecio Santos, _New York University_|Sketching Methods for Efficient Correlated Dataset Search \[[Details](#talk-by-aecio-santos)\]|
|10/4|Hung Ngo, _RelationalAI_|Query Optimization for Worst-case Optimal Joins|
|10/11|(Break)||
|10/18|Ippokratis Pandis, _Amazon_|Reinventing Cloud Analytics with Machine Learning \[[Details](#talk-by-ippokratis-pandis)\]|
|10/25|Raul Castro Fernandez, _University of Chicago_|The Value of Data and the Design of Data Markets \[[Details](#talk-by-raul-castro-fernandez)\]|
|11/1|Subarna Chatterjee, _Harvard University_|Cosine: A Cloud-Cost Optimized Self-Designing Key-Value Storage Engine \[[Details](#talk-by-subarna-chatterjee)\]|
|11/8|Arun Kumar, _University of California San Diego_|New DBification of ML/AI \[[Details](#talk-by-arun-kumar)\]|
|11/15|Arnab Nandi, _Ohio State University_|TBD|
|11/22|_MongoDB_|TBD|
|11/29|Matthias Boehm, _TU Berlin_|Optimizing Compiler Infrastructure for Data-centric ML Pipelines|

# Talk Details

## Talk by Aecio Santos

### Abstract

Dataset search is emerging as a critical capability in both research and industry: it has spurred many novel applications such as data augmentation for enriching data analyses and improving machine learning models. In this talk, we present our recent work that explores a new class of dataset search queries that uncovers data relationships in large table collections. In particular, we focus on join-correlation queries: given an input query table, find the top-k tables that are both joinable with it and contain columns strongly correlated with a column in the query table. Unfortunately, a naïve approach to evaluate these queries, which first finds joinable tables and then explicitly materializes joins and computes correlations between the query and all discovered tables, is prohibitively expensive. To solve this problem, we 1) present novel data sketching methods that enable the construction of an index for a large number of tables and that provide accurate estimates for join-correlation queries, and 2) explore different indexing and scoring strategies that effectively retrieve and rank the query results based on how well the columns are correlated with the query.

### Bio

Aécio Santos is a Research Engineer in the Visualization, Imaging, and Data Analysis (VIDA) group at New York University (NYU). He received a Master's Degree in Computer Science from the Federal University of Minas Gerais (in Brazil) and is currently a part-time Ph.D. candidate at New York University under the supervision of Prof. Juliana Freire. Over the years, he has worked, both in academia and industry, on a wide range of problems related to web crawling, news recommendation and classification, automated machine learning, and dataset search. He has served as a reviewer and has published papers at multiple premier data management and information retrieval conferences and journals such as VLDB, SIGMOD, WWW, WSDM, SIGIR, and CIKM.

## Talk by Ippokratis Pandis

### Abstract

Amazon Redshift is Amazon's Amazon's petabyte-scale data warehouse service. Over the recent years, Amazon Redshift has gone through a major rearchitecture, while remaining the most popular and highest performing cloud data warehouse service. One of the major elements of this rearchitecture has been the substantial use of machine learning in multiple areas of the service, with the culmination of the autonomics efforts being the introduction of Amazon Redshift Serverless offering. This talk presents the basic elements of Amazon Redshift's rearchitecture and then focuses on the different ways where machine learning is being used in Redshift to improve its operational health, efficiency, performance and cost. We close with the presentation of Amazon Redshift Serverless and its intelligent compute management layer.

### Bio

Ippokratis Pandis is a VP/Distinguished Engineer at Amazon Web Services. He spends most of his time on AWS's Analytics services, especially Amazon Redshift. Redshift is Amazon's fully managed, petabyte-scale data warehouse service. Previously, Ippokratis has held positions as software engineer at Cloudera where he worked on the Impala SQL-on-Hadoop query engine, and as member of the research staff at the IBM Almaden Research Center, where he worked on IBM DB2 BLU. Ippokratis received his PhD from the ECE department at Carnegie Mellon University. He is the recipient of a Test-of-Time award at EDBT 2019. He is the General Chair of SIGMOD 2023 and the president of HPTS.

## Talk by Raul Castro Fernandez

### Abstract

While data and artificial intelligence are driving many changes to our economic, social, political, financial, and legal systems, we know surprisingly little about their foundations and governing dynamics. In this talk, I will argue that the value of data arises from data markets, environments where agents exchange data. I will illustrate the importance of studying data markets and show several examples of where today’s data markets fall short and cause negative impacts on welfare and privacy. Then, I will suggest that data markets can be deliberately designed to avoid those pitfalls and present a proposal to advance the field that consists of two steps: data market design and data market platform implementation. I will illustrate the above points with examples of existing and future data markets. Finally, I will propose there exists a connection between the study of the value and economics of data and the discipline of data science. I will convey the importance of studying the data economy and the many tools and approaches the data management community has to contribute to this area.

### Bio

I am an assistant professor at the University of Chicago. My interests are in data: data science and data management. My group studies data markets and the value and economics of data. We work on designing well-functioning data markets and implementing data market platforms where those designs can be deployed. We also work on more traditional data management problems such as data discovery, integration, and processing. Before UChicago, I did a postdoc at MIT and completed my Ph.D. at Imperial College London.

## Talk by Subarna Chatterjee

### Abstract

We present a self-designing key-value storage engine, Cosine, which can take the shape of the close to “perfect” engine architecture given an input workload, a cloud budget, a target performance, and required cloud SLAs. By identifying and formalizing the first principles of storage engine layouts and core key-value algorithms, Cosine constructs a massive design space comprising of sextillion (10^36) possible storage engine designs over a diverse space of hardware and cloud pricing policies for three cloud providers – AWS, GCP, and Azure. Cosine spans across diverse designs such as Log-Structured Merge (LSM)-trees, B-trees, Log-Structured Hash (LSH)-tables, in-memory accelerators for filters and indexes as well as trillions of hybrid designs that do not appear in the literature or industry but emerge as valid combinations of the above. Cosine includes a unified distribution-aware I/O model and a learned concurrency-aware CPU model that can calculate the performance and cloud cost of running a workload on any possible design and hardware. Cosine can then search through that space in interactive times to find the best design and materializes the actual code of the resulting storage engine design using a templated Rust implementation. We demonstrate that on average Cosine outperforms state-of-the-art storage engines such as LSM-based RocksDB, BTree-based WiredTiger, and LSH-based FASTER by 23x, 25x, and 20x, respectively, for diverse workloads, data sizes, and cloud budgets across all YCSB core workloads and many variants.

### Bio

I am a post-doctoral researcher working with Prof. Stratos Idreos at Data Systems laboratory at Harvard University since January 2019. Before that I was a post-doctoral researcher (2017-2018) with the Myriads team at Inria, Rennes in France. I did my Ph.D. from Indian Institute of Technology Kharagpur, India from 2013-2017. Broadly speaking, I work on data science with my research focus centering around different sub-directions at different times in my career.

## Talk by Arun Kumar

### Abstract

The recent boom in ML/AI applications has brought into sharp focus the pressing need for tackling the concerns of scalability, usability, and manageability across the entire lifecycle of ML/AI applications. The ML/AI world has long studied the concerns of accuracy, automation, etc. from theoretical and algorithmic vantage points. But to truly democratize ML/AI, the vantage point of building and deploying practical systems is equally critical.

In this talk, I will make the case that it is high time to bridge the gap between the ML/AI world and a world that exemplifies successful democratization of data technology: databases. I will show how new bridges rooted in the principles, techniques, and tools of the database world are helping tackle the above pressing concerns and in turn, posing new research questions to the world of ML/AI. As case studies of such bridges, I will describe two lines of work from my group: query optimization for scalable deep learning systems and benchmarking data preparation in AutoML platforms. I will conclude with my thoughts on community mechanisms to foster more such bridges between research worlds and between research and practice.

### Bio

Arun Kumar is an Associate Professor in Computer Science and Engineering and the Halicioglu Data Science Institute at the University of California, San Diego. His primary research interests are in data management and systems for ML/AI-based data analytics. Systems and ideas from his work have been released as part of the Apache MADlib open-source library and shipped as part of products from or used internally by many database, Web, and cloud companies. He is a recipient of three SIGMOD research paper awards, five distinguished reviewer/metareviewer awards from SIGMOD/VLDB, the IEEE TCDE Rising Star Award, and an NSF CAREER Award.
