## Welcome to the VU Amsterdam - storage-systems wiki!
We will collect and grow the reading list for the Storage Systems class (https://animeshtrivedi.github.io/course-stosys/) at VU Amsterdam. ***All lecture slides are publically available.***

Hands-on wiki with commands and setup is available here: https://github.com/animeshtrivedi/storage-systems-wiki-reading-list/wiki

**Contributions:** please open a pull request with 1-2 line description of the paper! 

## Reading list 

### NVM storage and device-level details 
  * 

### Flash FTL designs, patterns, and GC designs 
  * 

### Host interfacing, OS and Storage I/O Stack  
  * Theano Stavrinos, Daniel S. Berger, Ethan Katz-Bassett, and Wyatt Lloyd. 2021. Don't be a blockhead: zoned namespaces make work on conventional SSDs obsolete. In Proceedings of the Workshop on Hot Topics in Operating Systems (HotOS '21). Association for Computing Machinery, New York, NY, USA, 144–151. https://doi.org/10.1145/3458336.3465300
     * ZNS is the new and exciting interface for NVM storage. It is also quite fundamental as the paper argues that it solves or makes old problems with flash useless. A good fun read (plus, summarizes a decade worth of research effort in managing flash)  
  * FlatFlash: Exploiting the Byte-Accessibility of SSDs within a Unified Memory-Storage Hierarchy, ASPLOS 2019, https://dl-acm-org.vu-nl.idm.oclc.org/doi/abs/10.1145/3297858.3304061

### Flash I/O Scheduling and quality-of-service/multi-tenancy 
  * 

### File Systems 
  * 

### Key-Value Storage 
  * Stratos Idreos and Mark Callaghan. 2020. Key-Value Storage Engines. In Proceedings of the 2020 ACM SIGMOD International Conference on Management of Data (SIGMOD '20). Association for Computing Machinery, New York, NY, USA, 2667–2672. https://doi.org/10.1145/3318464.3383133 
     * A small write up summarizing (2020) the current popular indexing structures about KV data structures 
  * Designing Access Methods: The RUM Conjecture (Read, Update, and Memory): https://stratos.seas.harvard.edu/files/stratos/files/rum.pdf
     * A good fundamental work that discusses that a single data structure cannot provide most optimal performance for all three types of operations 

### Storage Virtualization 
  *  

### Reliability and failures studies  
  * 

### Programmable storage, acceleration, offloading, computational storage  
  * 

### Persistent Memories 
  * 

### Netwoked/distributed Flash 
  * 

### Distributed/Cloud systems 
  * 

### NVM stroage and Energy consumption 
  * 

### NVM + Energy 
  * Bryan Harris and Nihat Altiparmak. When poll is more energy efficient than interrupt. In Proceedings of the 14th ACM Workshop on Hot Topics in Storage and File Systems, HotStorage ’22, page 59–64, New York, NY, USA, 2022. Association for Computing Machinery.  https://www.hotstorage.org/2022/slides/hotstorage22-paper44-presentation_slides.pdf

  * Bryan Harris and Nihat Altiparmak. Ultra‐low latency ssds’ impact on overall energy efficiency. In Proceedings of the 12th USENIX Conference on Hot Topics in Storage and File Systems, HotStorage’20, USA, 2020. USENIX Association. https://www.usenix.org/system/files/hotstorage20-paper61-slides-harris.pdf


  * Jing Li, Anirudh Badam, Ranveer Chandra, Steven Swanson, Bruce Worthington, and Qi Zhang. On the energy overhead of mobile storage systems. In Proceedings of the 12th USENIX Conference on File and Storage Technologies, FAST’14, page 105–118, USA, 2014. USENIX Association.

  * Jayashree Mohan, Dhathri Purohith, Mathew Halpern, Vijay Chidambaram, and Vijay Janapa Reddi. Storage on your smartphone uses more energy than you think. In Proceedings of the 9th USENIX Conference on Hot Topics in Storage and File Systems, HotStorage’17, page 9, USA, 2017. USENIX Association.

### Timeseries databases
  * Jalal Mostafa, Sara Wehbi, Suren Chilingaryan, Andreas Kopmann. 2022. SciTS: A Benchmark for Time-Series Databases in Scientific Experiments and Industrial Internet of Things. https://arxiv.org/abs/2204.09795v2
      * Paper describing a system for benchmarking the performance of timeseries databases. The paper generates data used to benchmark the performance of insertion and uses a few queries to test the performance of the querying engines.

### Good surveys 
  * Krijn Doekemeijer, Animesh Trivedi - Key-Value Stores on Flash Storage Devices: A Survey, https://arxiv.org/abs/2205.07975, May 2022.   
  * Athanasios Fevgas, Leonidas Akritidis, Panayiotis Bozanis, and Yannis Manolopoulos. 2020. Indexing in flash storage devices: a survey on challenges, current approaches, and future trends. <i>The VLDB Journal</i> 29, 1 (Jan 2020), 273–311. https://doi.org/10.1007/s00778-019-00559-8 https://link.springer.com/content/pdf/10.1007/s00778-019-00559-8.pdf  
     * One of the most comprehensive and well-written surveys on indexing data structures on flash storage 


### Misc. 
