# About

The Cornell Database Seminar covers recent research in the database area. The seminar meets weekly from 1 to 2 PM EST. All talks by external speakers are **public** and can be attended via Zoom (link [here](https://cornell.zoom.us/j/94791289427?pwd=c2grd2dvc2xnWHpuLzMvemNub3BPZz09)). Talk recordings, without Q&A, will be available [online](https://www.youtube.com/playlist?list=PLXPbT_PYOiRiTnsNRm0ojyXIbPVVe1iqi). The seminar is organized by the [Cornell Database Group](https://itrummer.github.io/dbgrouphp/).

# Schedule

|Date|Speaker|Talk|
|---|----- | ------- |
|2/7|Manos Athanassoulis, _Boston University_ | (A Prelude to) Building Robust LSM-based Key-Value Stores \[[Details](#talk-by-manos-athanassoulis)\] |
|2/14|Rolando Garcia Sanchez, _UC Berkeley_ | FLOR: Managing the Infinite Virtual Metadata of Model Training |
|2/21| Immanuel Trummer, _Cornell University_| |
|2/28| (Break) | |
|3/7|Carsten Binnig, _TU Darmstadt_ | Learned DBMS Components 2.0: From Workload-Driven to Zero-Shot Learning \[[Details](#talk-by-carsten-binnig)\]|
|3/14|Ibrahim Sabek, _MIT_ | LSched: A Workload-Aware Learned Query Scheduler for Analytical Database Systems |
|3/21|Volker Markl, _TU Berlin_ | Mosaics of Big Data: Database Systems and Information Management – Trends and a Vision \[[Details](#talk-by-volker-markl)\]|
|3/28|Davide Mottin, _Aarhus University_ | Cleaning Knowledge Graphs with Little Effort \[[Details](#talk-by-davide-mottin)\]|
|4/4|(Break)| |
|4/11|Laurel Orr, _Stanford University_ | |
|4/18|Angelos-Christos Anadiotis, _Ecole Polytechnique_| |
|4/25|Eugene Wu, _Columbia University_| |
|5/2|Roger Waleffe, _University of Wisconsin-Madison_| |
|5/9|Joe Hellerstein, _UC Berkeley_| |

# Talk Details

## Talk by Manos Athanassoulis

### Abstract

Log-structured merge (LSM) trees are becoming the de facto standard for write-intensive storage layers for both production NoSQL data stores and relational systems. As LSM-based systems are used by various applications and deployed in shared infrastructure (e.g., public or private cloud), they are tasked to support a number of requirements varying from performance, to cost, and privacy, being robust to external requirements and the inherent workload unpredictability. At the heart of any LSM-based engine, we have the background re-organization mechanism (or compaction), the behavior of which affects essentially every aspect of the LSM-tree including write amplification, write throughput, point and range lookup performance, space amplification, and delete performance. In this presentation, we will first introduce in detail the design space of LSM compactions and discuss their tradeoffs, we will then take a deep dive on a new family of delete-aware compactions. We will define as a design goal the delete persistence latency, and discuss how to bound it. Finally, we will discuss the importance of tuning in the presence of uncertainty and present a sneak-peek of a new methodology for near-optimal LSM tuning in the presence of uncertainty of the expected workload vs. the observed one.

### Bio

Manos Athanassoulis is an Assistant Professor of Computer Science at Boston University, Director and Founder of the BU Data-intensive Systems and Computing Laboratory and co-director of the BU Massive Data Algorithms and Systems Group. His research is in the area of data management focusing on building data systems that efficiently exploit modern hardware (computing units, storage, and memories), are deployed in the cloud, and can adapt to the workload both at setup time and, dynamically, at runtime. Before joining Boston University, Manos was a postdoc at Harvard University, earlier he obtained his PhD from EPFL, Switzerland, and spent one summer at IBM Research, Watson. Manos’ work has been recognized by awards like “Best of SIGMOD” in 2016, “Best of VLDB” in 2010 and 2017, and “Most Reproducible Paper” at SIGMOD in 2017, and has been supported by NSF and industry funds including a Facebook Faculty Research Award and gifts from Cisco and Red Hat.

## Talk by Rolando Garcia

## Talk by Immanuel Trummer

## Talk by Carsten Binnig

### Abstract

Database management systems (DBMSs) are the backbone for managing large volumes of data efficiently and thus play a central role in business and science today. For providing high per- formance, many of the most complex DBMS components such as query optimizers or schedulers involve solving non-trivial problems. To tackle such problems, very recent work has outlined a new direction of so-called learned DBMS components where core parts of DBMSs are being replaced by machine learning (ML) models which has shown to provide significant performance benefits. However, a major drawback of the current workload-driven learning approaches to enable learned DBMS components is that they not only cause very high overhead for training an ML model to replace a DBMS component but that the overhead occurs repeatedly which renders these approaches far from practical.

Hence, in this talk we present our vision to tackle the high costs and inflexibility of workload-driven learning called Learned DBMS Components 2.0. First, we introduce data-driven learning where the idea is to learn the data distribution over a complex relational schema. In contrast to workload-driven learning, no large workload has to be executed on the database to gather training data. While data-driven learning has many applications such as cardinality estimation or approximate query processing, many DBMS tasks such as physical cost estimation cannot be supported. We thus propose a second technique called zero-shot learning which is a general paradigm for learned DBMS components. Here, the idea is to train models that generalize to unseen data sets out-of-the-box. The idea is to train a model that has observed a variety of workloads on different data sets and can thus generalize. Initial results on the task of physical cost estimation suggest the feasibility of this approach. Finally, we discuss further opportunities which are enabled by zero-shot learning.

## Talk by Ibrahim Sabek

## Talk by Volker Markl

### Abstract

The global database research community has greatly impacted the functionality and performance of data storage and processing systems along the dimensions that define “big data”, i.e., volume, velocity, variety, and veracity. Locally, over the past five years, we have also been working on varying fronts. Among our contributions are: (1) establishing a vision for a database-inspired big data analytics system, which unifies the best of database and distributed systems technologies, and augments it with concepts drawn from compilers (e.g., iterations) and data stream processing, as well as (2) forming a community of researchers and institutions to create the Stratosphere platform to realize our vision. One major result from these activities was Apache Flink, an open-source big data analytics platform and its thriving global community of developers and production users. Although much progress has been made, when looking at the overall big data stack, a major challenge for database research community still remains. That is, how to maintain the ease-of-use despite the increasing heterogeneity and complexity of data analytics, involving specialized engines for various aspects of an end-to-end data analytics pipeline, including, among others, graph-based, linear algebra-based, and relational-based algorithms, and the underlying, increasingly heterogeneous hardware and computing infrastructure. 

At TU Berlin, DFKI, and the Berlin Institute for Foundations of Learning and Data (BIFOLD) we currently aim to advance research in this field via the Nebula Stream and Agora projects. Our goal is to remedy some of the heterogeneity challenges that hamper developer productivity and limit the use of data science technologies to just the privileged few, who are coveted experts. In this talk, we will outline how state-of-the-art SPEs have to change to exploit the new capabilities of the IoT and showcase how we tackle IoT challenges in our own system, NebulaStream. We will also present our vision for Agora, an asset ecosystem that provides the technical infrastructure for offering and using data and algorithms, as well as physical infrastructure components. 

### Bio

Volker Markl is a German Professor of Computer Science. He leads the Chair of Database Systems and Information Management at TU Berlin and the Intelligent Analytics for Massive Data Research Department at DFKI. In addition, he is Director of the Berlin Institute for the Foundations of Learning and Data (BIFOLD). He is a database systems researcher, conducting research at the intersection of distributed systems, scalable data processing, and machine learning. Volker led the Stratosphere project, which resulted in the creation of Apache Flink. Volker has received numerous honors and prestigious awards, including two ACM SIGMOD Research Highlight Awards and best paper awards at ACM SIGMOD, VLDB, ICDE, and EDBT. He was recognized as ACM Fellow for his contributions to query optimization, scalable data processing, and data programmability. He is a member of the Berlin-Brandenburg Academy of Sciences. In 2014, he was elected one of Germany's leading “Digital Minds“ (Digitale Köpfe) by the German Informatics Society.  He also is a member of the Berlin-Brandenburg Academy of Sciences and serves as advisor to academic institutions, governmental organizations, and technology companies. Volker holds eighteen patents and has been co-founder and mentor to several startups.


## Talk by Davide Mottin

### Abstract

Is it possible to assess whether the information in a database is true? This task is an important tile in the current misinformation era. Towards this goal, the talk introduces the task of Knowledge validation taking knowledge graph, one of the data models that are used for fact-checking. Knowledge graphs are graphs of entities (e.g., US, Joe Biden) connected through relationships (e.g., isPresidentOf). A typical approach to ensure data quality in the presence of continuous changes is to apply logic rules. These rules are automatically mined from the data using frequency-based approaches. As a result, these approaches depend on the data quality of the KG and are susceptible to errors and incompleteness. This talk shows a different approach we recently devised in which the domain expert is a first-class citizen in the validation process. To ensure a smooth and easy validation we devised a method that selects triples to validate in the quest for cleaner data. 

### Bio

Davide Mottin is an Assistant Professor at Aarhus University with expertise in graph mining, exploratory methods, and knowledge graphs.
Before joining Aarhus University he was a postdoctoral researcher at Hasso Plattner Institute, leading the graph mining subgroup in the Knowledge Discovery and Data Mining group. He has pioneered methods for Exploratory Analysis on knowledge graphs, graph embedding methods, and user-in-the-loop techniques for data management. 
He received his PhD in 2015 from the University of Trento. He was also visiting Yahoo! Labs in Barcelona, and Microsoft Research Asia in Beijing.

## Talk by Laurel Orr
