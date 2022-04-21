# About

The Cornell Database Seminar covers recent research in the database area. The seminar meets weekly from 1 to 2 PM ET. All talks by external speakers are **public** and can be attended via Zoom (link [here](https://cornell.zoom.us/j/94791289427?pwd=c2grd2dvc2xnWHpuLzMvemNub3BPZz09)). Talk recordings, without Q&A, will be available [online](https://www.youtube.com/playlist?list=PLXPbT_PYOiRiTnsNRm0ojyXIbPVVe1iqi). The seminar is organized by the [Cornell Database Group](https://itrummer.github.io/dbgrouphp/).

# Schedule

|Date|Speaker|Talk|
|---|----- | ------- |
|2/7|Manos Athanassoulis, _Boston University_ | (A Prelude to) Building Robust LSM-based Key-Value Stores \[[Details](#talk-by-manos-athanassoulis)\] \[[Video](https://t.co/ywgitHApbY)\]|
|2/14|Rolando Garcia Sanchez, _UC Berkeley_ | FLOR: Managing the Infinite Virtual Metadata of Model Training \[[Details](#talk-by-rolando-garcia-sanchez)\] \[[Video](https://youtu.be/gAhqAHnJme0)\]|
|2/21| Immanuel Trummer, _Cornell University_| Towards Tuning Tools that "Read" the Manual \[[Details](#talk-by-immanuel-trummer)\] \[[Video](https://youtu.be/rICyXhjyqp8)\]|
|2/28| (Break) | |
|3/7|Carsten Binnig, _TU Darmstadt_ | Learned DBMS Components 2.0: From Workload-Driven to Zero-Shot Learning \[[Details](#talk-by-carsten-binnig)\] \[[Video](https://youtu.be/7Ws_Ms4wVcc)\]|
|3/14|Ibrahim Sabek, _MIT_ | LSched: A Workload-Aware Learned Query Scheduler for Analytical Database Systems \[[Details](#talk-by-ibrahim-sabek)\] \[[Video](https://youtu.be/uiMdErKz_rk)\]|
|3/21|Volker Markl, _TU Berlin_ | Mosaics of Big Data: Database Systems and Information Management – Trends and a Vision \[[Details](#talk-by-volker-markl)\] \[[Video](https://youtu.be/Y0qq1Di-Qvc)\]|
|3/28|Davide Mottin, _Aarhus University_ | Cleaning Knowledge Graphs with Little Effort \[[Details](#talk-by-davide-mottin)\] \[[Video](https://youtu.be/l1O9EFmAXaM)\]|
|4/4|(Break)| |
|4/11|Laurel Orr, _Stanford University_ | Incremental Entity Embedding Maintenance in Foundation Model Ecosystems \[[Details](#talk-by-laurel-orr)\] \[[Video](https://youtu.be/IgKz5Rnjnvk)\] |
|4/18|Angelos-Christos Anadiotis, _Ecole Polytechnique_| Pursue of Conflicts of Interest Across Heterogeneous Data \[[Details](#talk-by-angelos-christos-anadiotis)\] \[[Video](https://youtu.be/Qwc68qj4bK8)\] |
|4/25|Eugene Wu, _Columbia University_| Systems for Human Data Interaction \[[Details](#talk-by-eugene-wu)\] |
|5/2|Roger Waleffe, _University of Wisconsin-Madison_| Training Graph Neural Networks over Billion-Scale Graphs on a Single Machine \[[Details](#talk-by-roger-waleffe)\] |
|5/9|Joe Hellerstein, _UC Berkeley_| |

# Talk Details

## Talk by Manos Athanassoulis

### Abstract

Log-structured merge (LSM) trees are becoming the de facto standard for write-intensive storage layers for both production NoSQL data stores and relational systems. As LSM-based systems are used by various applications and deployed in shared infrastructure (e.g., public or private cloud), they are tasked to support a number of requirements varying from performance, to cost, and privacy, being robust to external requirements and the inherent workload unpredictability. At the heart of any LSM-based engine, we have the background re-organization mechanism (or compaction), the behavior of which affects essentially every aspect of the LSM-tree including write amplification, write throughput, point and range lookup performance, space amplification, and delete performance. In this presentation, we will first introduce in detail the design space of LSM compactions and discuss their tradeoffs, we will then take a deep dive on a new family of delete-aware compactions. We will define as a design goal the delete persistence latency, and discuss how to bound it. Finally, we will discuss the importance of tuning in the presence of uncertainty and present a sneak-peek of a new methodology for near-optimal LSM tuning in the presence of uncertainty of the expected workload vs. the observed one.

### Bio

Manos Athanassoulis is an Assistant Professor of Computer Science at Boston University, Director and Founder of the BU Data-intensive Systems and Computing Laboratory and co-director of the BU Massive Data Algorithms and Systems Group. His research is in the area of data management focusing on building data systems that efficiently exploit modern hardware (computing units, storage, and memories), are deployed in the cloud, and can adapt to the workload both at setup time and, dynamically, at runtime. Before joining Boston University, Manos was a postdoc at Harvard University, earlier he obtained his PhD from EPFL, Switzerland, and spent one summer at IBM Research, Watson. Manos’ work has been recognized by awards like “Best of SIGMOD” in 2016, “Best of VLDB” in 2010 and 2017, and “Most Reproducible Paper” at SIGMOD in 2017, and has been supported by NSF and industry funds including a Facebook Faculty Research Award and gifts from Cisco and Red Hat.

## Talk by Rolando Garcia Sanchez

### Abstract

There’s lots to log in model training: time series of metrics, tensor histograms, embeddings, activations, and more. Surprisingly though, most of the time, model developers only log parameters (e.g. batch size and learning rate) and time series metrics (e.g. loss and accuracy). What do they do when they need more data than the little bit they logged? They add more logging statements, and they re-run training. We call this practice “Hindsight Logging” because of its retrospective quality. In this talk, I will discuss efficient hindsight logging using Fast Low-Overhead Recovery (FLOR), a record-replay system first presented at VLDB ’21. During my talk, I will give a demo of FLOR using VSCode and a Jupyter Notebook, and show how I can use it, together with integrated query support, to understand what alternatives my colleague has tried to fit an NLP model for a Kaggle competition.

### Bio

Rolando is a PhD candidate at UC Berkeley advised by Joe Hellerstein. He studies and builds systems to manage the training context and vast metadata of machine learning. Rolando received his B.S. in computer science from Arizona State University, and he is a recipient of the NSF graduate research fellowship, and UC Berkeley’s Chancellor’s fellowship. 

## Talk by Immanuel Trummer

### Abstract

The Internet offers a plethora of database tuning hints, formulated in natural language and published in manuals, blog entries, or discussion forums. Traditionally, such text is used to educate human database administrators exclusively. However, recent advances in natural language processing (NLP) enable automated tuning tools to benefit from such hints as well. 
In this talk, I discuss DB-BERT, a system that combines information gained from text analysis with information gained via trial runs. DB-BERT is guided by a reinforcement learning algorithm and uses pre-trained language models to analyse text. I present first experimental results for DB-BERT and discuss avenues for extensions. Finally, I discuss novel applications of NLP in the context of database tuning more broadly.

### Bio

Immanuel Trummer is assistant professor at Cornell University, working towards making data analysis more efficient and more user-friendly. His papers were selected for “Best of VLDB”, “Best of SIGMOD”, for the ACM SIGMOD Research Highlight Award, and for publication in CACM as CACM Research Highlight. His current research is funded by the NSF and by multiple Google Faculty Research Awards. 

## Talk by Carsten Binnig

### Abstract

Database management systems (DBMSs) are the backbone for managing large volumes of data efficiently and thus play a central role in business and science today. For providing high per- formance, many of the most complex DBMS components such as query optimizers or schedulers involve solving non-trivial problems. To tackle such problems, very recent work has outlined a new direction of so-called learned DBMS components where core parts of DBMSs are being replaced by machine learning (ML) models which has shown to provide significant performance benefits. However, a major drawback of the current workload-driven learning approaches to enable learned DBMS components is that they not only cause very high overhead for training an ML model to replace a DBMS component but that the overhead occurs repeatedly which renders these approaches far from practical.

Hence, in this talk we present our vision to tackle the high costs and inflexibility of workload-driven learning called Learned DBMS Components 2.0. First, we introduce data-driven learning where the idea is to learn the data distribution over a complex relational schema. In contrast to workload-driven learning, no large workload has to be executed on the database to gather training data. While data-driven learning has many applications such as cardinality estimation or approximate query processing, many DBMS tasks such as physical cost estimation cannot be supported. We thus propose a second technique called zero-shot learning which is a general paradigm for learned DBMS components. Here, the idea is to train models that generalize to unseen data sets out-of-the-box. The idea is to train a model that has observed a variety of workloads on different data sets and can thus generalize. Initial results on the task of physical cost estimation suggest the feasibility of this approach. Finally, we discuss further opportunities which are enabled by zero-shot learning.

## Talk by Ibrahim Sabek

### Abstract

Query scheduling is a crucial task for analytical database systems that can greatly affect query latency. However, existing scheduling approaches are either based on heuristics or not able to learn a scheduling policy that considers the database-specific characteristics (e.g., operator types, pipelining). As a result, such approaches become not efficient for analytical database systems. In this talk, we introduce LSched: a fully learned workload-aware query scheduler for in-memory analytical database systems. LSched provides an efficient inter-query and intra-query scheduling for dynamic analytical workloads (i.e., different queries can arrive/depart at any time). We integrated LSched with an efficient in-memory analytical database system, and evaluated it with TPCH, SSB, and JOB benchmarks. Our evaluation shows the efficiency of LSched in both streaming and batching query workloads.

### Bio

Ibrahim Sabek is a postdoctoral associate at MIT CSAIL, and a member of the MIT Data Systems Group working with Tim Kraska and Michael Cafarella. He completed his PhD in computer science from University of Minnesota, Twin Cities in 2020. Recently, he has been named a Computing Innovation Fellow (CIFellow) by the Computing Research Association (CRA) and the National Science Foundation (NSF). He also received the University-wide Best Dissertation Honorable Mention in 2021 for his PhD work. He is interested in exploring machine learning for data systems, with a special focus on query execution and scheduling. For more information, please check this website: http://people.csail.mit.edu/ibrahimsabek/.

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

### Abstract

There is a paradigm shift in machine learning pipelines where hand-turned downstream model pipelines are being replace by “foundation model ecosystems”. Foundation models are large, commoditized architectures trained on massive corpora without any manual labels or features. Once pretrained, foundation models can be adapted to numerous downstream systems, resulting in higher quality downstream systems that are easier to maintain. One critical application of foundation models is their use in pretraining embeddings for entities in a knowledge base that are then integrated into systems such as QA, recommendation, and data integration. As entities are continuously being updated and added to a knowledge base, an outstanding challenge is how to update the entity embeddings to encode any new updates without having to pay the high cost of retraining the model from scratch.

This talk will have two parts. In the first, I will introduce foundation model ecosystems and why they are fundamentally changing the way in which engineers build and train models. In the second part, I will dive into the challenge of how to maintain and update entity embeddings in these foundation model ecosystems.

### Bio

Laurel Orr is currently a PostDoc at Stanford working with Chris Ré in the Hazy Research Lab. In August of 2019, she graduated with a PhD from Paul G Allen School for Computer Science and Engineering at the University of Washington in Seattle. She was part of the Database Group and advised by Dan Suciu and Magdalena Balazinska. She was a 2020 winner of the IC Postdoc Research Fellowship Program and one of the 2015 winners of the NSG GRFP in Compute Science.

Her research interests are broadly at the intersection of machine learning and data management. She focuses on how to manage the end-to-end lifecycle of self-supervised embedding pipelines. This includes problems of how to better train, maintain, monitor, and patch the embedding models and their use downstream.

## Talk by Angelos-Christos Anadiotis

### Abstract

According to the French transparency law, a conflict of interest is any situation where a public interest may interfere with a public or private interest, in such a way that the public interest may be, or appear to be, unduly influenced. Discovering conflicts of interest is a tedious task, as it requires the exploration of several data sources, including both structured and unstructured data, in order to discover connections among entities that could be problematic. Investigative journalism has been actively involved in the pursue of conflicts of interest, and the investigation may take years in order to sort out all the data sources needed and then process the data that they include. This talk addresses the problem of finding connections among entities that belong to heterogeneous data sources, in a scalable manner. It describes an end-to-end pipeline which integrates the heterogeneous data in a graph and then discovers connections among nodes in the graph that correspond to a given set of keywords. The work has been carried out in collaboration with several researchers, most notably: Ioana Manolescu, Oana Balalau, Helena Galhardas, and many others. More details on the project can be found here: https://sourcessay.inria.fr.

### Bio

Angelos Christos Anadiotis is Assistant Professor of Computer Science at Ecole Polytechnique, Palaiseau, France. He is a member of the joint INRIA-Ecole Polytechnique, CEDAR team, led by Ioana Manolescu. His research focuses on scalable data processing in the face of data, workload, and hardware heterogeneity. Throughout his career, he has received funding from national, international, and industrial sources.

## Talk by Eugene Wu

### Abstract

The rapid democratization of data has placed its access and analysis in the hands of the entire population. While the advances in rapid and large-scale data processing continue to reduce runtimes and costs, the interfaces and tools for end-users to interact with, and work with, data is still lacking.  It is still too difficult to translate a user’s data needs into the appropriate interfaces, too difficult to develop data intensive interfaces that are responsive and scalable, and too difficult for users to understand and interpret the data they see. In this talk, I will provide an overview of our lab's recent work on systems for human data interaction that go towards addressing these challenges.

### Bio

Eugene Wu is broadly interested in technologies that help users play with their data. His goal is for users at all technical levels to effectively and quickly make sense of their information. He is interested in solutions that ultimately improve the interface between users and data, and uses techniques borrowed from fields such as data management, systems, crowd sourcing, visualization, and HCI. Eugene Wu received his Ph.D. from MIT, B.S. from Cal, and was a postdoc in the AMPLab. 

Eugene Wu has received the VLDB 2018 10-year test of time award, best-of-conference citations at ICDE and VLDB, the SIGMOD 2016 best demo award, the NSF CAREER, and the Google and Amazon faculty awards.

## Talk by Roger Waleffe

### Abstract

In this talk, I will present Marius++, a system for resource optimized training of Graph Neural Networks (GNNs) on a single machine. To support billion-scale graphs, Marius++ utilizes pipelined mini-batch training and the entire memory hierarchy, including disk. This architecture requires Marius++ to address two main challenges. First, Marius++ optimizes GNN mini-batch preparation and processing to make it as efficient as possible on a machine with fixed resources. Second, Marius++ employs techniques to utilize disk storage during training without bottlenecking throughput or hurting model accuracy. This talk will highlight how Marius++ with one GPU can achieve the same level of model accuracy up to 8x faster than existing industrial systems when they are using up to eight GPUs. By scaling training using disk storage, Marius++ deployments on billion-scale graphs are up to 64x cheaper in monetary cost than those of the competing systems.

### Bio

Roger Waleffe is a third year PhD student at the University of Wisconsin-Madison working under the supervision of Prof. Theodoros Rekatsinas. His work focuses on the intersection of systems and algorithmic challenges for training large-scale ML models using the full memory hierarchy. Roger is coleading the Marius project (https://marius-project.org/) which aims to make the use of Graph Neural Networks and Graph Embeddings over billion scale graphs easier, faster, and cheaper. Roger holds a B.S. in computer science and physics from UW-Madison and is a recipient of the UW-Madison departmental graduate research fellowship and Goldwater scholarship.
