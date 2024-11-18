# Welcome to the VU Amsterdam - storage-systems wiki!
We will collect and grow the reading list for the Storage Systems class (https://atlarge-research.com/courses/storage-systems-vu/) at VU Amsterdam. 
  * All course material is publically available (slides, assignments, coding framework).   
  * ***All lecture slides are publically available.***
  * Hands-on wiki with commands and setup is available here: https://github.com/animeshtrivedi/storage-systems-wiki-reading-list/wiki
  * We are also collecting nice surveys we can find: https://github.com/stonet-research/storage-systems-wiki-reading-list#a-selection-of-storage-related-surveys 

***

If you find material from the class useful, then consider citing our work as [PDF](https://atlarge-research.com/pdfs/2024-stosys-education.pdf): 

> **Reviving Storage Systems Education in the 21st Century — An experience report**, Animesh Trivedi, Matthijs Jansen, Krijn Doekemeijer, Sacheendra Talluri, Nick Tehrany (2024 May) In 2024 IEEE/ACM 24rd International Symposium on Cluster, Cloud and Internet Computing (CCGrid'24), https://www.computer.org/csdl/proceedings-article/ccgrid/2024/956600a616/20ShedG8GeQ.

```
@INPROCEEDINGS {2024-ccgrid-stosys-experience,
author = { Trivedi, Animesh and Jansen, Matthijs and Doekemeijer, Krijn and Talluri, Sacheendra and Tehrany, Nick },
booktitle = { 2024 IEEE 24th International Symposium on Cluster, Cloud and Internet Computing (CCGrid) },
title = { Reviving Storage Systems Education in the 21st Century — An experience report },
year = {2024},
volume = {},
ISSN = {},
pages = {616-625},
doi = {10.1109/CCGrid59990.2024.00074},
url = {https://doi.ieeecomputersociety.org/10.1109/CCGrid59990.2024.00074},
publisher = {IEEE Computer Society},
address = {Los Alamitos, CA, USA},
month = {May}
}
```
***

**Contributions:** please open a pull request with 1-2 line description of the paper! 

## Table of Content 
1. [NVM storage, introduction, device-level details](#1-nvm-storage-introduction-device-level-details)
2. [Host interfacing, OS and Storage I/O Stack](#2-host-interfacing-os-and-storage-io-stack)
3. [SSD internals (FTL, GC, buffering, staging, scheduling)](#3-ssd-internals-ftl-gc-buffering-staging-scheduling)
4. [NVMe, Flash, PMEM, SSD File Systems](#4-nvme-flash-pmem-ssd-file-systems)
5. [Key-Value Storage and Caches](#5-key-value-storage-and-caches)
6. [Persistent Memories / disaggregation / CXL](#6-persistent-memories--disaggregation--cxl)
7. [Networked/distributed Flash/NVMoF/Storage Disaggregation](#7-networkeddistributed-flashnvmofstorage-disaggregation)
8. [Programmable storage, acceleration, offloading, computational storage, workload-specific storage](#8-programmable-storage-acceleration-offloading-computational-storage-workload-specific-storage)
9. [Storage Virtualization, Emulation, Simulation](#9-storage-virtualization-emulation-simulation)
10. [Flash I/O Scheduling and quality-of-service/multi-tenancy](#10-flash-io-scheduling-and-quality-of-servicemulti-tenancy)
11. [Reliability and failures studies](#11-reliability-and-failures-studies)
12. [Graphs Storage and Processing Systems](#12-graphs-storage-and-processing-systems)
13. [Performance, Efficiency, Scalability](#13-performance-efficiency-scalability)
14. [NVM storage and Energy consumption](#14-nvm-storage-and-energy-consumption)
15. [Database, Timeseries, VectorDB, Lookup, Indexes on Storage](#15-database-timeseries-vectordb-lookup-indexes-on-storage)
16. [Emerging systems architectures](#16-emerging-systems-architectures)
17. [Emerging storage interfaces and features](#17-emerging-storage-interfaces-and-features)
18. [SNIA/NVMe weblinks](#18-snianvme-weblinks)
19. [Benchmarking, traces, profiling, monitoring, and characterization](#19-benchmarking-traces-profiling-monitoring-and-characterization)
20. [RAID, Compression, De-duplication](#20-raid-compression-de-duplication)
21. [ML and (Storage) Systems](#21-ml-and-storage-systems)
22. [A selection of storage related surveys](#22-a-selection-of-storage-related-surveys)

## 1. NVM storage, introduction, device-level details  
  * Michael Cornwell. 2012. Anatomy of a Solid-state Drive: While the ubiquitous SSD shares many features with the hard-disk drive, under the surface they are completely different. Queue 10, 10 (October 2012), 30–36. https://doi.org/10.1145/2381996.2385276
  * Mihir Nanavati, Malte Schwarzkopf, Jake Wires, and Andrew Warfield. 2015. Non-volatile Storage: Implications of the Datacenter’s Shifting Center. Queue 13, 9 (November-December 2015), 33–56. https://doi.org/10.1145/2857274.2874238
  * Ethan Miller, Achilles Benetopoulos, George Neville-Neil, Pankaj Mehra, and Daniel Bittman. 2023. Pointers in Far Memory: A rethink of how data and computations should be organized. Queue 21, 3, Pages 50 (May/June 2023), 19 pages. https://doi.org/10.1145/3606029
  
## 2. Host interfacing, OS and Storage I/O Stack 
  * PAIO: General, Portable I/O Optimizations With Minor Application Modifications, https://www.usenix.org/conference/fast22/presentation/macedo 
  * ScalaCache: Scalable User-Space Page Cache Management with Software-Hardware Coordination, https://www.usenix.org/conference/atc24/presentation/peng
  * Don't be a blockhead: zoned namespaces make work on conventional SSDs obsolete. In Proceedings of the Workshop on Hot Topics in Operating Systems (HotOS '21). Association for Computing Machinery, New York, NY, USA, 144–151. https://doi.org/10.1145/3458336.3465300    
  * FlatFlash: Exploiting the Byte-Accessibility of SSDs within a Unified Memory-Storage Hierarchy. In Proceedings of the Twenty-Fourth International Conference on Architectural Support for Programming Languages and Operating Systems (ASPLOS '19). Association for Computing Machinery, New York, NY, USA, 971–985. https://doi.org/10.1145/3297858.3304061
  * Foreactor: Exploiting Storage I/O Parallelism with Explicit Speculation. arXiv:2409.01580. https://arxiv.org/abs/2409.01580
  * sRoute: Treating the Storage Stack Like a Network, https://www.usenix.org/conference/fast16/technical-sessions/presentation/stefanovici
  * Improving Flash Storage Performance by Caching Address Mapping Table in Host Memory, https://www.usenix.org/conference/hotstorage17/program/presentation/jeong
  * Open Compute Project, Flash Storage, https://www.smartm.com/technology/open-compute-project-ocp-v1-0
    > NVMe Cloud SSD Specification, https://www.opencompute.org/documents/nvme-cloud-ssd-specification-v1-0-3-pdf
    > Datacenter NVMe® SSD Specification, https://www.opencompute.org/documents/datacenter-nvme-ssd-specification-v2-0r21-pdf
 
## 3. SSD internals (FTL, GC, buffering, staging, scheduling)
  * HMB-SSD: Framework for Efficient Exploiting of the Host Memory Buffer in the NVMe SSD, https://ieeexplore.ieee.org/abstract/document/8868151 
  * Improving Flash Storage Performance by Caching Address Mapping Table in Host Memory, https://www.usenix.org/conference/hotstorage17/program/presentation/jeong 
  * Fantastic SSD internals and how to learn and use them. In Proceedings of the 15th ACM International Conference on Systems and Storage (SYSTOR '22). Association for Computing Machinery, New York, NY, USA, 72–84. https://doi.org/10.1145/3534056.3534940 
  * LavaStore: ByteDance’s Purpose-built, High-performance, Cost-effective Local Storage Engine for Cloud Services, https://www.vldb.org/pvldb/vol17/p3799-jiao.pdf 
  *  Jinghan Sun, Shaobo Li, Yunxin Sun, Chao Sun, Dejan Vucinic, and Jian Huang. 2023. LeaFTL: A Learning-Based Flash Translation Layer for Solid-State Drives. In Proceedings of the 28th ACM International Conference on Architectural Support for Programming Languages and Operating Systems, Volume 2 (ASPLOS 2023). Association for Computing Machinery, New York, NY, USA, 442–456. https://doi.org/10.1145/3575693.3575744
  * Aayush Gupta, Youngjae Kim, and Bhuvan Urgaonkar. 2009. DFTL: a flash translation layer employing demand-based selective caching of page-level address mappings. In Proceedings of the 14th international conference on Architectural support for programming languages and operating systems (ASPLOS XIV). Association for Computing Machinery, New York, NY, USA, 229–240. https://doi.org/10.1145/1508244.1508271
  * S. Jiang, Lei Zhang, XinHao Yuan, Hao Hu and Yu Chen, "S-FTL: An efficient address translation for flash memory by exploiting spatial locality," 2011 IEEE 27th Symposium on Mass Storage Systems and Technologies (MSST), Denver, CO, 2011, pp. 1-12, doi: 10.1109/MSST.2011.5937215.
  * You Zhou, Fei Wu, Ping Huang, Xubin He, Changsheng Xie, and Jian Zhou. 2015. An efficient page-level FTL to optimize address translation in flash memory. In Proceedings of the Tenth European Conference on Computer Systems (EuroSys '15). Association for Computing Machinery, New York, NY, USA, Article 12, 1–16. https://doi.org/10.1145/2741948.2741949
  * LearnedFTL: A Learning-Based Page-Level FTL for Reducing Double Reads in Flash-Based SSDs, https://doi.ieeecomputersociety.org/10.1109/HPCA57654.2024.00054  
  * Rino Micheloni, Alessia Marelli, and Kam Eshghi. 2012. Inside Solid State Drives (SSDs). Springer Publishing Company, Incorporated. https://dl.acm.org/doi/10.5555/2412028 

## 4. NVMe, Flash, PMEM, SSD File Systems 
  * Ziggurat: A Tiered File System for Non-Volatile Main Memories and Disks, https://www.usenix.org/conference/fast19/presentation/zheng
  * FStream: Managing Flash Streams in the File System, https://www.usenix.org/conference/fast18/presentation/rho   

## 5. Key-Value Storage and Caches 
  * vLSM: Low tail latency and I/O amplification in LSM-based KV stores, https://arxiv.org/abs/2407.15581, 2024. 
  * Calcspar: A Contract-Aware LSM Store for Cloud Storage with Low Latency Spikes, https://www.usenix.org/conference/atc23/presentation/zhou
  * The CacheLib Caching Engine: Design and Experiences at Scale, https://www.usenix.org/conference/osdi20/presentation/berg
  * Structural Designs Meet Optimality: Exploring Optimized LSM-tree Structures in a Colossal Configuration Space. Proc. ACM Manag. Data 2, 3, Article 175 (June 2024), 26 pages. https://doi.org/10.1145/3654978
  * MirrorKV: An Efficient Key-Value Store on Hybrid Cloud Storage with Balanced Performance of Compaction and Querying, https://dl.acm.org/doi/10.1145/3626736.     
  * Key-Value Storage Engines. In Proceedings of the 2020 ACM SIGMOD International Conference on Management of Data (SIGMOD '20). Association for Computing Machinery, New York, NY, USA, 2667–2672. https://doi.org/10.1145/3318464.3383133 
     * A small write up summarizing (2020) the current popular indexing structures about KV data structures 
  * Designing Access Methods: The RUM Conjecture (Read, Update, and Memory): https://stratos.seas.harvard.edu/files/stratos/files/rum.pdf
     * A good fundamental work that discusses that a single data structure cannot provide most optimal performance for all three types of operations
  * https://www.vldb.org/pvldb/vol14/p2216-sarkar.pdf, Constructing and Analyzing the LSM Compaction Design Space
  * DComp: Efficient Offload of LSM-tree Compaction with Data Processing Units, https://dl.acm.org/doi/abs/10.1145/3605573.3605633 
  * SpanDB: A Fast, Cost-Effective LSM-tree Based KV Store on Hybrid Storage, Hao Chen, University of Science and Technology of China & Qatar Computing Research Institute, HBKU; Chaoyi Ruan and Cheng Li, University of Science and Technology of China; Xiaosong Ma, Qatar Computing Research Institute, HBKU; Yinlong Xu, University of Science and Technology of China & Anhui Province Key Laboratory of High Performance Computing, https://www.usenix.org/conference/fast21/presentation/chen-hao 
  * Ruisong Zhou, Yuzhan Zhang, Chunhua Li, Ke Zhou, Peng Wang, Gong Zhang, Ji Zhang, Guangyu Zhang. 2024. HyperDB: a Novel Key Value Store for Reducing Background Traffic in Heterogeneous SSD Storage. In Proceedings of the 53rd International Conference on Parallel Processing. https://dl.acm.org/doi/10.1145/3673038.3673153
  * Hao Wang, Jiaxin Ou, Ming Zhao, Sheng Qiu, Yizheng Jiao, Yi Wang, Qizhong Mao, Zhengyu Yang, Yang Liu, Jianshun Zhang et al. 2024. LavaStore: ByteDance’s Purpose-built, High-performance, Cost-effective Local Storage Engine for Cloud Services. PVLDB 17(12). https://www.vldb.org/pvldb/vol17/p3799-jiao.pdf
  * Raja Appuswamy, Goetz Graefe, Renata Borovica-Gajic, and Anastasia Ailamaki. 2019. The five-minute rule 30 years later and its impact on the storage hierarchy. Commun. ACM 62, 11 (November 2019), 114–120. https://doi.org/10.1145/3318163
    > https://infoscience.epfl.ch/server/api/core/bitstreams/2c459c6d-3672-4dc2-b1db-2e94d140ed09/content 

## 6. Persistent Memories / disaggregation / CXL 
  * An Examination of CXL Memory Use Cases for In-Memory Database Management Systems using SAP HANA MINSEON AHN (SAP Labs Korea)*; Thomas Willhalm (Intel Deutschland GmbH); Norman May (SAP SE); Donghun Lee (SAP Labs Korea); Suprasad Mutalik Desai (Intel); Daniel Booss (SAP SE); Jungmin Kim (SAP); Navneet Singh (Intel Technology India Pvt Ltd); Daniel Ritter (SAP); Oliver Rebholz (SAP SE), https://www.vldb.org/pvldb/vol17/p3827-ahn.pdf
  * Bolong Zheng, Yongyong Gao, Jingyi Wan, Lingsen Yan, Long Hu, Bo Liu, Yunjun Gao, Xiaofang Zhou, and Christian S. Jensen. 2023. DecLog: Decentralized Logging in Non-Volatile Memory for Time Series Database Systems. Proc. VLDB Endow. 17, 1 (September 2023), 1–14. https://doi.org/10.14778/3617838.3617839
  * Ying Zheng and Kian-Lee Tan. 2024. Sorting on Byte-Addressable Storage: The Resurgence of Tree Structure. Proc. VLDB Endow. 17, 6 (February 2024), 1487–1500. https://doi.org/10.14778/3648160.3648185
  * BonsaiKV: Towards Fast, Scalable, and Persistent Key-Value Stores with Tiered, Heterogeneous Memory System. Proc. VLDB Endow. 17, 4 (December 2023), 726–739. https://doi.org/10.14778/3636218.3636228
  * FluidKV: Seamlessly Bridging the Gap between Indexing Performance and Memory-Footprint on Ultra-Fast Storage. Proc. VLDB Endow. 17, 6 (February 2024), 1377–1390. https://doi.org/10.14778/3648160.3648177
  * CXL and the Return of Scale-Up Database Engines. Proc. VLDB Endow. 17, 10 (June 2024), 2568–2575. https://doi.org/10.14778/3675034.3675047
  * Anchor: A Library for Building Secure Persistent Memory Systems. Proc. ACM Manag. Data 1, 4, Article 231 (December 2023), 31 pages. https://doi.org/10.1145/3626718. 
  * Scalable Distributed Inverted List Indexes in Disaggregated Memory. Proc. ACM Manag. Data 2, 3, Article 171 (June 2024), 27 pages. https://doi.org/10.1145/3654974
  * Persistent Memory Research in the Post-Optane Era. In Proceedings of the 1st Workshop on Disruptive Memory Systems (DIMES '23). Association for Computing Machinery, New York, NY, USA, 23–30. https://doi.org/10.1145/3609308.3625268
  * A Comprehensive Empirical Study of File Systems on Optane Persistent Memory, https://ieeexplore.ieee.org/abstract/document/9605448 
  * TPP: Transparent Page Placement for CXL-Enabled Tiered-Memory. In Proceedings of the 28th ACM International Conference on Architectural Support for Programming Languages and Operating Systems, Volume 3 (ASPLOS 2023). Association for Computing Machinery, New York, NY, USA, 742–755. https://doi.org/10.1145/3582016.3582063 
  * Pond: CXL-Based Memory Pooling Systems for Cloud Platforms. In Proceedings of the 28th ACM International Conference on Architectural Support for Programming Languages and Operating Systems, Volume 2 (ASPLOS 2023). Association for Computing Machinery, New York, NY, USA, 574–587. https://doi.org/10.1145/3575693.3578835 
  * Cache in Hand: Expander-Driven CXL Prefetcher for Next Generation CXL-SSD. In Proceedings of the 15th ACM Workshop on Hot Topics in Storage and File Systems (HotStorage '23). Association for Computing Machinery, New York, NY, USA, 24–30. https://doi.org/10.1145/3599691.3603406 
  * Hello bytes, bye blocks: PCIe storage meets compute express link for memory expansion (CXL-SSD). In Proceedings of the 14th ACM Workshop on Hot Topics in Storage and File Systems (HotStorage '22). Association for Computing Machinery, New York, NY, USA, 45–51. https://doi.org/10.1145/3538643.3539745 
  * Jianguo Wang and Qizhen Zhang. 2023. Disaggregated Database Systems. In Companion of the 2023 International Conference on Management of Data (SIGMOD '23). Association for Computing Machinery, New York, NY, USA, 37–44. https://doi.org/10.1145/3555041.3589403 
  * Hasan Al Maruf and Mosharaf Chowdhury. 2023. Memory Disaggregation: Advances and Open Challenges. SIGOPS Oper. Syst. Rev. 57, 1 (June 2023), 29–37. https://doi.org/10.1145/3606557.3606562 
  * Marcos K. Aguilera, Emmanuel Amaro, Nadav Amit, Erika Hunhoff, Anil Yelam, and Gerd Zellweger. 2023. Memory disaggregation: why now and what are the challenges. SIGOPS Oper. Syst. Rev. 57, 1 (June 2023), 38–46. https://doi.org/10.1145/3606557.3606563
  * Direct Access, High-Performance Memory Disaggregation with DirectCXL, https://www.usenix.org/conference/atc22/presentation/gouk
  * FlatFS: Flatten Hierarchical File System Namespace on Non-volatile Memories, https://www.usenix.org/conference/atc22/presentation/cai 
  * Poseidon: Safe, Fast and Scalable Persistent Memory Allocator (Middleware, 2020), https://dl.acm.org/doi/10.1145/3423211.3425671 
  * Persistent State Machines for Recoverable In-memory Storage Systems with NVRam,  https://www.usenix.org/conference/osdi20/presentation/zhang-wen
  * Wenda Tang, Ying Han, Tianxiang Ai, Guanghui Li, Bin Yu, Xin Yang. 2024. Yggdrasil: Reducing Network I/O Tax with (CXL-Based) Distributed Shared Memory. In Proceedings of the 53rd International Conference on Parallel Processing. https://dl.acm.org/doi/10.1145/3673038.3673138
  * Qizhen Zhang, Philip A. Bernstein, Badrish Chandramouli, Jiasheng Hu, Yiming Zheng. 2024. DDS: DPU-optimized Disaggregated Storage. PVLDB, 17(11). https://www.vldb.org/pvldb/vol17/p3304-zhang.pdf 
  * Minseon Ahn, Willhalm Thomas, Norman May, Donghun Lee, Suprasad Mutalik Desai, Daniel Booss, Jungmin Kim, Navneet Singh, Daniel Ritter, Oliver Rebholz. 2024. An Examination of CXL Memory Use Cases for In-Memory Database Management Systems using SAP HANA. PVLDB, 17(12). https://www.vldb.org/pvldb/vol17/p3827-ahn.pdf
  * SPMFS: A Scalable Persistent Memory File System on Optane Persistent Memory. In Proceedings of the 50th International Conference on Parallel Processing (ICPP '21). Association for Computing Machinery, New York, NY, USA, Article 3, 1–10. https://doi.org/10.1145/3472456.3472503
  * A Survey of Non-Volatile Main Memory File Systems, https://jcst.ict.ac.cn/en/article/pdf/preview/10.1007/s11390-023-1054-3.pdf (https://link.springer.com/article/10.1007/s11390-023-1054-3) 
  * Ziggurat: A Tiered File System for Non-Volatile Main Memories and Disks https://www.usenix.org/conference/fast19/presentation/zheng
    > FileBench, RocksDB, SQLite, MySQL
  * Characterizing the performance of intel optane persistent memory: a close look at its on-DIMM buffering. In Proceedings of the Seventeenth European Conference on Computer Systems (EuroSys '22). Association for Computing Machinery, New York, NY, USA, 488–505. https://doi.org/10.1145/3492321.3519556
  * "CFFS: A Persistent Memory File System for Contiguous File Allocation With Fine-Grained Metadata," in IEEE Access, vol. 10, pp. 91678-91698, 2022, doi: 10.1109/ACCESS.2022.3202532 https://ieeexplore.ieee.org/abstract/document/9869672 


## 7. Networked/distributed Flash/NVMoF/Storage Disaggregation   
  * Towards Resource Efficiency: Practical Insights into Large-Scale Spark Workloads at ByteDance. PVLDB, 17(12): 3759-3771, 2024. doi:10.14778/3685800.3685804
  * DDS: DPU-Optimized Disaggregated Storage. Proc. VLDB Endow. 17, 11 (July 2024), 3304–3317. https://doi.org/10.14778/3681954.3682002
  * DPC: DPU-accelerated High-Performance File System Client. In Proceedings of the 53rd International Conference on Parallel Processing. https://dl.acm.org/doi/10.1145/3673038.3673123
  * Understanding the Performance Implications of the Design Principles in Storage-Disaggregated Databases. Proc. ACM Manag. Data 2, 3, Article 180 (June 2024), 26 pages. https://doi.org/10.1145/3654983
  * CaaS-LSM: Compaction-as-a-Service for LSM-based Key-Value Stores in Storage Disaggregated Infrastructure. Proc. ACM Manag. Data 2, 3, Article 124 (June 2024), 28 pages. https://doi.org/10.1145/3654927 
  * RackBlox: A Software-Defined Rack-Scale Storage System with Network-Storage Co-Design, https://dl.acm.org/doi/10.1145/3600006.3613170
  * Impact of Commodity Networks on Storage Disaggregation with NVMe-oF (2021) https://par.nsf.gov/servlets/purl/10299229 (https://dl.acm.org/doi/10.1007/978-3-030-71058-3_3) 
  * NVMe-oAF: Towards Adaptive NVMe-oF for IO-Intensive Workloads on HPC Cloud. In Proceedings of the 31st International Symposium on High-Performance Parallel and Distributed Computing (HPDC '22). Association for Computing Machinery, New York, NY, USA, 56–70. https://doi.org/10.1145/3502181.3531476
  * Performance Characterization of NVMe-over-Fabrics Storage Disaggregation. ACM Trans. Storage 14, 4, Article 31 (November 2018), 18 pages. https://doi.org/10.1145/3239563
  * Optimizing the Ceph Distributed File System for High Performance Computing, http://csl.snu.ac.kr/papers/pdp19.pdf 


## 8. Programmable storage, acceleration, offloading, computational storage, workload-specific storage
  * BPF-oF: Storage Function Pushdown Over the Network, https://arxiv.org/abs/2312.06808, 2023.  
  * Breathing New Life into an Old Tree: Resolving Logging Dilemma of B+-tree on Modern Computational Storage Drives. Proc. VLDB Endow. 17, 2 (October 2023), 134–147. https://doi.org/10.14778/3626292.3626297
  * PreSto: An In-Storage Data Preprocessing System for Training Recommendation Models, https://ieeexplore.ieee.org/document/10609715 (ISCA 2024) 
  * DeepStore: In-Storage Acceleration for Intelligent Queries. In Proceedings of the 52nd Annual IEEE/ACM International Symposium on Microarchitecture (MICRO '52). Association for Computing Machinery, New York, NY, USA, 224–238. https://doi.org/10.1145/3352460.3358320 
  * Alberto Lerner and Philippe Bonnet. 2021. Not your Grandpa's SSD: The Era of Co-Designed Storage Devices. In Proceedings of the 2021 International Conference on Management of Data (SIGMOD '21). Association for Computing Machinery, New York, NY, USA, 2852–2858. https://doi.org/10.1145/3448016.3457540
  * DAPHNE: An Open and Extensible System Infrastructure for Integrated Data Analysis Pipelines, https://pure.itu.dk/ws/files/86467917/CIDR2022.pdf 
  * Computational Storage: Where Are We Today? https://www.cidrdb.org/cidr2021/papers/cidr2021_paper29.pdf  
  * Cognitive SSD: A Deep Learning Engine for In-Storage Data Retrieval, https://www.usenix.org/conference/atc19/presentation/liang 
  * POLARDB Meets Computational Storage: Efficiently Support Analytical Workloads in Cloud-Native Relational Database, https://www.usenix.org/conference/fast20/presentation/cao-wei
  * A Fast and Flexible Hardware-based Virtualization Mechanism for Computational Storage Devices, https://www.usenix.org/conference/atc21/presentation/kwon
  * Leveraging Computational Storage for Power-Efficient Distributed Data Analytics. ACM Trans. Embed. Comput. Syst. 21, 6, Article 82 (November 2022), 36 pages. https://doi.org/10.1145/3528577 
  * Cost-effective, Energy-efficient, and Scalable Storage Computing for Large-scale AI Applications. ACM Trans. Storage 16, 4, Article 21 (November 2020), 37 pages. https://doi.org/10.1145/3415580 
  * SmartSAGE: training large-scale graph neural networks using in-storage processing architectures. In Proceedings of the 49th Annual International Symposium on Computer Architecture (ISCA '22). Association for Computing Machinery, New York, NY, USA, 932–945. https://doi.org/10.1145/3470496.3527391
  * An Analytical Model-based Capacity Planning Approach for Building CSD-based Storage Systems. ACM Trans. Embed. Comput. Syst. Just Accepted (September 2023). https://doi.org/10.1145/3623677
  * Scalable Billion-point Approximate Nearest Neighbor Search Using SmartSSDs, https://www.usenix.org/conference/atc24/presentation/tian

## 9. Storage Virtualization, Emulation, Simulation
  * MQsim (simulator): https://www.usenix.org/system/files/conference/fast18/fast18-tavakkol.pdf
  * FEMU (emulator): https://www.usenix.org/system/files/conference/fast18/fast18-li.pdf
  * NVMeVirt (emulator): https://www.usenix.org/conference/fast23/presentation/kim-sang-hoon
  * Amber https://ieeexplore.ieee.org/abstract/document/8574562  and for ZNS: https://ieeexplore.ieee.org/abstract/document/996440
  * vFPIO: A Virtual I/O Abstraction for FPGA-accelerated I/O Devices, Jiyang Chen, Harshavardhan Unnibhavi, Atsushi Koshiba, and Pramod Bhatotia, https://www.usenix.org/conference/atc24/presentation/chen-jiyang
  * Wear distributions in FF-SSD: https://dl.acm.org/doi/abs/10.1145/3538643.3539757 
  * Nameless writes had an emulator. How does it work? https://www.usenix.org/legacy/event/fast12/tech/full_papers/Zhang2-7-12.pdf 
     > Goliath allows evaluating large (1TB at that time) workloads on small disks without performance gaps.
  * MDev-NVMe (mediated passthrough): https://www.usenix.org/system/files/conference/atc18/atc18-peng.pdf
  *  Analyzing, modeling, and provisioning QoS for NVMe ssds: https://ieeexplore.ieee.org/abstract/document/8603171/
  *  Spdk vhost-nvme (user-space): Accelerating i/os in virtual machines on nvme ssds via user space vhost target: https://ieeexplore.ieee.org/abstract/document/8567374/
  *  FlashBlox: https://www.usenix.org/system/files/conference/fast17/fast17_huang.pdf

## 10. Flash I/O Scheduling and quality-of-service/multi-tenancy 
  * Huaicheng Li, Martin L. Putra, Ronald Shi, Xing Lin, Gregory R. Ganger, and Haryadi S. Gunawi. 2021. IODA: A Host/Device Co-Design for Strong Predictability Contract on Modern Flash Storage. In Proceedings of the ACM SIGOPS 28th Symposium on Operating Systems Principles (SOSP '21). Association for Computing Machinery, New York, NY, USA, 263–279. https://doi.org/10.1145/3477132.3483573
  * BlockFlex: Enabling Storage Harvesting with Software-Defined Flash in Modern Cloud Platforms, OSDI 2022. https://www.usenix.org/conference/osdi22/presentation/reidys 
  * FLIN: https://ieeexplore.ieee.org/abstract/document/8416843
  * D2FQ: Device-Direct Fair Queueing for NVMe SSDs, Jiwon Woo, Minwoo Ahn, Gyusun Lee, and Jinkyu Jeong, Sungkyunkwan University, https://www.usenix.org/system/files/fast21-woo.pdf
  * blk-switch: https://www.usenix.org/system/files/osdi21-hwang.pdf
  * Huaicheng Li, Martin L. Putra, Ronald Shi, Fadhil I. Kurnia, Xing Lin, Jaeyoung Do, Achmad Imam Kistijantoro, Gregory R. Ganger, and Haryadi S. Gunawi. 2023. Extending and Programming the NVMe I/O Determinism Interface for Flash Arrays. ACM Trans. Storage 19, 1, Article 5 (February 2023), 33 pages. https://doi.org/10.1145/3568427
  * I/O Schedulers for Proportionality and Stability on Flash-Based SSDs in Multi-Tenant Environments
  * Towards Low-Latency I/O Services for Mixed Workloads Using Ultra-Low Latency SSDs (FastResponse): https://dl.acm.org/doi/pdf/10.1145/3524059.3532378
  * Configuring and Coordinating End-to-end QoS for Emerging Storage Infrastructure. ACM Trans. Model. Perform. Eval. Comput. Syst. 9, 1, Article 4 (March 2024), 32 pages. https://doi.org/10.1145/3631606
  * Enabling NVMe WRR support in Linux Block Layer,https://www.usenix.org/conference/hotstorage17/program/presentation/joshi 
  * BFQ, Multiqueue-Deadline, or Kyber? Performance Characterization of Linux Storage Schedulers in the NVMe Era, https://dl.acm.org/doi/10.1145/3629526.3645053
  * Do we still need IO schedulers for low-latency disks? https://dl.acm.org/doi/10.1145/3599691.3603400
  * Heiner Litz, Javier Gonzalez, Ana Klimovic, and Christos Kozyrakis. 2022. RAIL: Predictable, Low Tail Latency for NVMe Flash. ACM Trans. Storage 18, 1, Article 5 (February 2022), 21 pages. https://doi.org/10.1145/3465406
  * Liuying Ma, Zhenqing Liu, Jin Xiong, Yue Wu, Renhai Chen, Xi Peng, Ying Zhang, Gong Zhang, Dejun Jiang. 2024. zQoS: Unleashing full performance capabilities of NVMe SSDs while enforcing SLOs in distributed storage systems. In Proceedings of the 53rd International Conference on Parallel Processing.
    https://dl.acm.org/doi/abs/10.1145/3673038.3673156
  * Shucheng Wang, Kaiye Zhou, Zhandong Guo, Qiang Cao, Jun Xu, Jie Yao. 2024. SIndex: An SSD-based Large-scale Indexing with Deterministic Latency for Cloud Block Storage. In Proceedings of the 53rd International Conference on Parallel Processing. https://dl.acm.org/doi/10.1145/3673038.3673041
  * Vivek Narasayya and Surajit Chaudhuri. 2022. Multi-Tenant Cloud Data Services: State-of-the-Art, Challenges and Opportunities. In Proceedings of the 2022 International Conference on Management of Data (SIGMOD '22). Association for Computing Machinery, New York, NY, USA, 2465–2473. https://doi.org/10.1145/3514221.3522566


## 11. Reliability and failures studies  
  * Flash Reliability in Production: The Expected and the Unexpected, https://www.usenix.org/conference/fast16/technical-sessions/presentation/schroeder 
  * Evaluating File System Reliability on Solid State Drives, https://www.usenix.org/conference/atc19/presentation/jaffer 
  * Operational Characteristics of SSDs in Enterprise Storage Systems: A Large-Scale Field Study, https://www.usenix.org/conference/fast22/presentation/maneas 
  * A Study of SSD Reliability in Large Scale Enterprise Storage Deployments, https://www.usenix.org/conference/fast20/presentation/maneas 
  * Multi-view Feature-based SSD Failure Prediction: What, When, and Why, https://www.usenix.org/conference/fast23/presentation/zhang 
  * NVMe SSD Failures in the Field: the Fail-Stop and the Fail-Slow, https://www.usenix.org/conference/atc22/presentation/lu
  * SSD Failures in Datacenters: What? When? and Why? In Proceedings of the 9th ACM International on Systems and Storage Conference (SYSTOR '16). Association for Computing Machinery, New York, NY, USA, Article 7, 1–11. https://doi.org/10.1145/2928275.2928278
  * Lessons and actions: what we learned from 10K SSD-related storage system failures. In Proceedings of the 2019 USENIX Conference on Usenix Annual Technical Conference (USENIX ATC '19). USENIX Association, USA, 961–975. https://www.usenix.org/conference/atc19/presentation/xu 
  * Understanding the Robustness of SSDs under Power Fault, https://www.usenix.org/conference/fast13/technical-sessions/presentation/zheng  
  * Error Characterization, Mitigation, and Recovery in Flash-Memory-Based Solid-State Drives, https://ieeexplore.ieee.org/document/8013174/1000 

## 12. Graphs Storage and Processing Systems 
  * **Collection of papers projects:** https://github.com/dnasc/graph-processing
  * **Graph Generators:** https://github.com/yuanqidu/awesome-graph-generation
  * **Search:** https://github.com/search?q=awesome-graph&type=repositories
  * Mosaic: Processing a Trillion-Edge Graph on a Single Machine. In Proceedings of the Twelfth European Conference on Computer Systems (EuroSys '17). Association for Computing Machinery, New York, NY, USA, 527–543. https://doi.org/10.1145/3064176.3064191
  * Efficient Large Graph Processing with Chunk-Based Graph Representation Model, https://www.usenix.org/conference/atc24/presentation/wang-rui 
  * Tarikul Islam Papon, Taishan Chen, Shuo Zhang, and Manos Athanassoulis. 2024. CAVE: Concurrency-Aware Graph Processing on SSDs. Proc. ACM Manag. Data 2, 3, Article 125 (June 2024), 26 pages. https://doi.org/10.1145/3654928 
  * Kiran Kumar Matam, Gunjae Koo, Haipeng Zha, Hung-Wei Tseng, and Murali Annavaram. 2019. GraphSSD: graph semantics aware SSD. In Proceedings of the 46th International Symposium on Computer Architecture (ISCA '19). Association for Computing Machinery, New York, NY, USA, 116–128. https://doi.org/10.1145/3307650.3322275  
  * FlashGraph: Processing Billion-Node Graphs on an Array of Commodity SSDs, https://www.usenix.org/conference/fast15/technical-sessions/presentation/zheng ([Github](https://github.com/flashxio/FlashX))
  * Juno Kim and Steven Swanson. 2022. Blaze: fast graph processing on fast SSDs. In Proceedings of the International Conference on High Performance Computing, Networking, Storage and Analysis (SC '22). IEEE Press, Article 44, 1–15. (Github: https://github.com/NVSL/blaze )
  * TriCache: A User-Transparent Block Cache Enabling High-Performance Out-of-Core Processing with In-Memory Programs, https://www.usenix.org/conference/osdi22/presentation/feng (has graph as one of the driving workloads) 
  * "A Structure-Aware Storage Optimization for Out-of-Core Concurrent Graph Processing," in IEEE Transactions on Computers, vol. 71, no. 7, pp. 1612-1625, 1 July 2022, doi: 10.1109/TC.2021.3098976.
  * "A Hybrid Update Strategy for I/O-Efficient Out-of-Core Graph Processing," in IEEE Transactions on Parallel and Distributed Systems, vol. 31, no. 8, pp. 1767-1782, 1 Aug. 2020, doi: 10.1109/TPDS.2020.2973143.
  * LUMOS: Dependency-Driven Disk-based Graph Processing, https://www.usenix.org/conference/atc19/presentation/vora [https://github.com/pdclab/lumos](https://github.com/pdclab/lumos)
  * GraphWalker: An I/O-Efficient and Resource-Friendly Graph Analytic System for Fast and Scalable Random Walks, https://www.usenix.org/conference/atc20/presentation/wang-rui
  * MBFGraph: An SSD-based External Graph System for Evolving Graphs. In Proceedings of the International Conference for High Performance Computing, Networking, Storage and Analysis (SC '23). Association for Computing Machinery, New York, NY, USA, Article 24, 1–13. https://doi.org/10.1145/3581784.3607070
  * GraFboost: using accelerated flash storage for external graph analytics. In Proceedings of the 45th Annual International Symposium on Computer Architecture (ISCA '18). IEEE Press, 411–424. https://doi.org/10.1109/ISCA.2018.00042
  * GLIST: Towards In-Storage Graph Learning, https://www.usenix.org/conference/atc21/presentation/li-cangyuan
  * Hardware/Software Co-Programmable Framework for Computational SSDs to Accelerate Deep Learning Service on Large-Scale Graphs, https://www.usenix.org/conference/fast22/presentation/kwon
  * GraFboost: using accelerated flash storage for external graph analytics. In Proceedings of the 45th Annual International Symposium on Computer Architecture (ISCA '18). IEEE Press, 411–424. https://doi.org/10.1109/ISCA.2018.00042
  * Load the edges you need: a generic I/O optimization for disk-based graph processing. In Proceedings of the 2016 USENIX Conference on Usenix Annual Technical Conference (USENIX ATC '16). USENIX Association, USA, 507–522.
  * Lambda-IO: A Unified IO Stack for Computational Storage, https://www.usenix.org/system/files/fast23-yang-zhe.pdf  
  * https://people.csail.mit.edu/jshun/graph.shtml
  * Graphene: Fine-Grained IO Management for Graph Computing, https://www.usenix.org/conference/fast17/technical-sessions/presentation/liu (Github:https://github.com/iHeartGraph/Graphene)
  * Seraph: Towards Scalable and Efficient Fully-external Graph Computation via On-demand Processing, https://www.usenix.org/conference/fast24/presentation/yang-tsun-yu
  * Parallelizing Sequential Graph Computations. In Proceedings of the 2017 ACM International Conference on Management of Data (SIGMOD '17). Association for Computing Machinery, New York, NY, USA, 495–510. https://doi.org/10.1145/3035918.3035942
  * Everything you always wanted to know about multicore graph processing but were afraid to ask, https://www.usenix.org/conference/atc17/technical-sessions/presentation/malicevic (https://github.com/jmalicevic/EverythingGraph) 

  
## 13. Performance, Efficiency, Scalability
  * I/O Passthru: Upstreaming a flexible and efficient I/O Path in Linux, https://www.usenix.org/system/files/fast24-joshi.pdf
  * Understanding modern storage APIs: a systematic study of libaio, SPDK, and io_uring. In Proceedings of the 15th ACM International Conference on Systems and Storage (SYSTOR '22). Association for Computing Machinery, New York, NY, USA, 120–127. https://doi.org/10.1145/3534056.3534945
  * What Modern NVMe Storage Can Do, and How to Exploit it: High-Performance I/O for High-Performance Storage Engines. Proc. VLDB Endow. 16, 9 (May 2023), 2090–2102. https://doi.org/10.14778/3598581.3598584
  * Performance Characterization of Modern Storage Stacks: POSIX I/O, libaio, SPDK, and io_uring. In Proceedings of the 3rd Workshop on Challenges and Opportunities of Efficient and Performant Storage Systems (CHEOPS '23). Association for Computing Machinery, New York, NY, USA, 35–45. https://doi.org/10.1145/3578353.3589545
  * Reducing Minor Page Fault Overheads through Enhanced Page Walker, https://dl.acm.org/doi/full/10.1145/3547142
  * BlockFlex: Enabling Storage Harvesting with Software-Defined Flash in Modern Cloud Platforms, https://www.usenix.org/conference/osdi22/presentation/reidys

## 14. NVM storage and Energy consumption   
  * Can Storage Devices be Power Adaptive? https://theanoli.github.io/files/hotstorage24-xie.pdf
  * EMPower: The Case for a Cloud Power Control Plane https://hotcarbon.org/assets/2024/pdf/hotcarbon24-final57.pdf
  * The carbon footprint of distributed cloud storage https://arxiv.org/abs/1803.06973 (2019)
  * On the Limitations of Carbon-Aware Temporal and Spatial Workload Shifting in the Cloud. In Proceedings of the Nineteenth European Conference on Computer Systems (EuroSys '24). Association for Computing Machinery, New York, NY, USA, 924–941. https://doi.org/10.1145/3627703.3650079
  * Energy Implications of IO Interface Design Choices. In Proceedings of the 15th ACM Workshop on Hot Topics in Storage and File Systems (HotStorage '23). Association for Computing Machinery, New York, NY, USA, 58–64. https://doi.org/10.1145/3599691.3603411 
  * When poll is more energy efficient than interrupt. In Proceedings of the 14th ACM Workshop on Hot Topics in Storage and File Systems, HotStorage ’22, page 59–64, New York, NY, USA, 2022. Association for Computing Machinery.  https://www.hotstorage.org/2022/slides/hotstorage22-paper44-presentation_slides.pdf
  * Ultra‐low latency ssds’ impact on overall energy efficiency. In Proceedings of the 12th USENIX Conference on Hot Topics in Storage and File Systems, HotStorage’20, USA, 2020. USENIX Association. https://www.usenix.org/system/files/hotstorage20-paper61-slides-harris.pdf
  * On the energy overhead of mobile storage systems. In Proceedings of the 12th USENIX Conference on File and Storage Technologies, FAST’14, page 105–118, USA, 2014. USENIX Association.
  * Storage on your smartphone uses more energy than you think. In Proceedings of the 9th USENIX Conference on Hot Topics in Storage and File Systems, HotStorage’17, page 9, USA, 2017. USENIX Association.
  * Hamming Tree: The Case for Energy-Aware Indexing for NVMs. In Proceedings of the ACM on Management of Data. SIGMOD'2023. ACM New York, NY, USA, 2023.
  * Treehouse: A Case For Carbon-Aware Datacenter Software. SIGENERGY Energy Inform. Rev. 3, 3 (October 2023), 64–70. https://doi.org/10.1145/3630614.3630626 


## 15. Database, Timeseries, VectorDB, Lookup, Indexes on Storage  
  * SingleStore-V: An Integrated Vector Database System in SingleStore, VLDB 2024, https://doi.org/10.14778/3685800.3685805 
  * Alexander van Renen, Dominik Horn, Pascal Pfeil, Kapil Vaidya, Wenjian Dong, Murali Narayanaswamy, Zhengchun Liu, Gaurav Saxena, Andreas Kipf, and Tim Kraska. 2024. Why TPC is Not Enough: An Analysis of the Amazon Redshift Fleet. Proc. VLDB Endow. 17, 11 (July 2024), 3694–3706. https://doi.org/10.14778/3681954.3682031
  * Apache TsFile: An IoT-native Time Series File Format, VLDB 2024. 
  * Cloud-Native Database Systems and Unikernels: Reimagining OS Abstractions for Modern Hardware. Proc. VLDB Endow. 17, 8 (April 2024), 2115–2122. https://doi.org/10.14778/3659437.3659462
  * An Empirical Evaluation of Columnar Storage Formats. Proc. VLDB Endow. 17, 2 (October 2023), 148–161. https://doi.org/10.14778/3626292.3626298
  * Are There Fundamental Limitations in Supporting Vector Data Management in Relational Databases? A Case Study of PostgreSQL. Proceedings of International Conference on Data Engineering (ICDE), 2024.
  * Vector Database Management Techniques and Systems. In Companion of the 2024 International Conference on Management of Data (SIGMOD/PODS '24). Association for Computing Machinery, New York, NY, USA, 597–604. https://doi.org/10.1145/3626246.3654691
  * Milvus: A Purpose-Built Vector Data Management System. In Proceedings of the 2021 International Conference on Management of Data (SIGMOD '21). Association for Computing Machinery, New York, NY, USA, 2614–2627. https://doi.org/10.1145/3448016.3457550
  * Vexless: A Serverless Vector Data Management System Using Cloud Functions. Proc. ACM Manag. Data 2, 3, Article 187 (June 2024), 26 pages. https://doi.org/10.1145/3654990
  * Limousine: Blending Learned and Classical Indexes to Self-Design Larger-than-Memory Cloud Storage Engines. Proc. ACM Manag. Data 2, 1, Article 47 (February 2024), 28 pages. https://doi.org/10.1145/3639302
    * We present Limousine, a self-designing key-value storage engine, that can automatically morph to the near-optimal storage engine architecture shape given a workload, a cloud budget, and target performance
  * Viktor Leis. 2024. LeanStore: A High-Performance Storage Engine for NVMe SSDs. PVLDB 17(12). https://www.vldb.org/pvldb/vol17/p4536-leis.pdf
  * What Modern NVMe Storage Can Do, And How To Exploit It: High-Performance I/O for High-Performance Storage Engines https://www.vldb.org/pvldb/vol16/p2090-haas.pdf
  * AirIndex: Versatile Index Tuning Through Data and Storage, https://dl.acm.org/doi/10.1145/3617308 
  * Starling: An I/O-Efficient Disk-Resident Graph Index Framework for High-Dimensional Vector Similarity Search on Data Segment. Proc. ACM Manag. Data 2, 1, Article 14 (February 2024), 27 pages. https://doi.org/10.1145/3639269
  * Chenguang Fang, Zijie Chen, Shaoxu Song, Xiangdong Huang, Chen Wang, and Jianmin Wang. 2024. On Reducing Space Amplification with Multi-Column Compaction in Apache IoTDB. Proc. VLDB Endow. 17, 11 (July 2024), 2974–2986. https://doi.org/10.14778/3681954.3681977
  * Time Series Representation for Visualization in Apache IoTDB. Proc. ACM Manag. Data 2, 1, Article 35 (February 2024), 26 pages. https://doi.org/10.1145/3639290
  * MOST: Model-Based Compression with Outlier Storage for Time Series Data, (SIGMOD 2023) https://dl.acm.org/doi/10.1145/3626737.
  * Jalal Mostafa, Sara Wehbi, Suren Chilingaryan, Andreas Kopmann. 2022. SciTS: A Benchmark for Time-Series Databases in Scientific Experiments and Industrial Internet of Things. https://arxiv.org/abs/2204.09795v2
  * * Peter Bailis, Camille Fournier, Joy Arulraj, and Andy Pavlo. 2016. Research for Practice: Distributed Consensus and Implications of NVM on Database Management Systems: Expert-curated Guides to the Best of CS Research. Queue 14, 3 (May-June 2016), 53–67. https://doi.org/10.1145/2956641.2967618


## 16. Emerging systems architectures 
  * https://hotinfra24.github.io/ 
    * > Designing Cloud Server for Lower Carbon
    * > Revisiting Distributed Programming in the CXL Era
    * > Lotus: Characterize Architecture Level CPU-based Preprocessing in Machine Learning Pipelines
  * https://hotinfra23.github.io/ 
    * > To virtualize or not to virtualize AI Infrastructure: A perspective, https://hotinfra23.github.io/papers/hotinfra23-paper16.pdf
    * > Memory Disaggregation: Open Challenges in the Era of CXL
    * > On the Discontinuation of Persistent Memory: Looking Back to Look Forward
    * > Building Next-Generation Software-Defined Data Centers with Network-Storage Co-Design
  * FpgaNIC: An FPGA-based Versatile 100Gb SmartNIC for GPUs https://www.usenix.org/system/files/atc22-wang-zeke.pdf 
  * CPU-free Computing: A Vision with a Blueprint. In Proceedings of the 19th Workshop on Hot Topics in Operating Systems (HOTOS '23). Association for Computing Machinery, New York, NY, USA, 1–14. https://doi.org/10.1145/3593856.3595906
  * Gabin Schieffer, Jacob Wahlgren, Jie Ren, Jennifer Faj, Ivy Peng. 2024. Harnessing Integrated CPU-GPU System Memory for HPC: a first look into Grace Hopper. In Proceedings of the 53rd International Conference on Parallel Processing. https://dl.acm.org/doi/10.1145/3673038.3673110

## 17. Emerging storage interfaces and features 

### 17.1 ZNS: Explanations, research directions and ZNS extensions
* Bjørling, M., Aghayev, A., Holmberg, H., Ramesh, A., Le Moal, D., Ganger, G. R., & Amvrosiadis, G. (2021). ZNS: Avoiding the Block Interface Tax for Flash-based SSDs. In 2021 USENIX Annual Technical Conference (USENIX ATC 21) (pp. 689-703). https://www.usenix.org/conference/atc21/presentation/bjorling
. An explanation of ZNS and what it is good for.
* Bjørling, M. (2019, February). From open-channel SSDs to zoned namespaces. In Proc. Linux Storage Filesyst. Conf.(Vault) (Vol. 1). https://www.usenix.org/sites/default/files/conference/protected-files/nsdi19_slides_bjorling.pdf The transition from open-channel to ZNS.
* Theano Stavrinos, Daniel S. Berger, Ethan Katz-Bassett, and Wyatt Lloyd. 2021. Don't be a blockhead: zoned namespaces make work on conventional SSDs obsolete. In Proceedings of the Workshop on Hot Topics in Operating Systems (HotOS '21). Association for Computing Machinery, New York, NY, USA, 144–151. https://doi.org/10.1145/3458336.3465300
* Append is Near: Log-based Data Management on ZNS SSDs. https://www.ssrc.ucsc.edu/media/pubs/8698b15f3152427d1285a995af615fbe7be26c7b.pdf Explanation of ZNS append operation, introduction of Group Append, advantages of alternatives, and various research directions for file systems, LSM-trees, databases and logs.
* Han, K., Gwak, H., Shin, D., & Hwang, J. (2021). ZNS+: Advanced zoned namespace interface for supporting in-storage zone compaction. In 15th USENIX Symposium on Operating Systems Design and Implementation (OSDI 21) (pp. 147-162). https://www.usenix.org/conference/osdi21/presentation/han A new LFS-aware ZNS interface, where the host can offload data copy operations to the SSD, and more functionalities that aids such file systems (threaded logging support).
* Maheshwari, U. (2021, July). From blocks to rocks: A natural extension of zoned namespaces. In Proceedings of the 13th ACM Workshop on Hot Topics in Storage and File Systems (pp. 21-27). https://dl.acm.org/doi/abs/10.1145/3465332.3470870 Extend ZNS with "rocks", support for variable-size pieces of data.
* Tehrany, N., & Trivedi, A. (2022). Understanding NVMe Zoned Namespace (ZNS) Flash SSD Storage Devices. arXiv preprint arXiv:2206.01547. https://arxiv.org/abs/2206.01547 A systemic analysis of integration options, current software support and initial performance measurements for ZNS.
* Bae, H., Kim, J., Kwon, M., & Jung, M. (2022, June). What you can't forget: exploiting parallelism for zoned namespaces. In Proceedings of the 14th ACM Workshop on Hot Topics in Storage and File Systems (pp. 79-85). https://dl.acm.org/doi/abs/10.1145/3538643.3539744 Discussion of ZNS benefits and how ZNS zone-to-zone relationships affect internal parallelism/performance, also how schedulers can solve such isssues.
* Zoned Namespaces Use Cases, Standard and Linux Ecosystem. Samsung, 2020 SNIA. https://www.snia.org/sites/default/files/SDCEMEA/2020/3%20-%20Javier%20Gonzalez%20Zoned%20namespacese.PDF 
* Renping Liu, Junhua Chen, Peng Chen, Linbo Long, Anping Xiong, Duo Liu. 2024. Hi-ZNS: High Space Efficiency and Zero-Copy LSM-tree-based Stores on ZNS SSDs. In Proceedings of the 53rd International Conference on Parallel Processing. https://dl.acm.org/doi/10.1145/3673038.3673096
* Choi, G., Lee, K., Oh, M., Choi, J., Jhin, J., & Oh, Y. (2020). A New LSM-style Garbage Collection Scheme for ZNS SSDs. In 12th USENIX Workshop on Hot Topics in Storage and File Systems (HotStorage 20). https://www.usenix.org/conference/hotstorage20/presentation/choi
* Oh, G., Yang, J., & Ahn, S. (2021). Efficient Key-Value Data Placement for ZNS SSD. Applied Sciences, 11(24), 11842. https://www.mdpi.com/2076-3417/11/24/11842
* Jung, J., & Shin, D. (2022, June). Lifetime-leveling LSM-tree compaction for ZNS SSD. In Proceedings of the 14th ACM Workshop on Hot Topics in Storage and File Systems (pp. 100-105). https://dl.acm.org/doi/abs/10.1145/3538643.3539741
* Bergman, S., Cassel, N., Bjørling, M., & Silberstein, M. (2022). ZNSwap:un-Block your Swap. In 2022 USENIX Annual Technical Conference (USENIX ATC 22) (pp. 1-18). https://www.usenix.org/conference/atc22/presentation/bergman
* Lee, H. R., Lee, C. G., Lee, S., & Kim, Y. (2022, June). Compaction-aware zone allocation for LSM based key-value store on ZNS SSDs. In Proceedings of the 14th ACM Workshop on Hot Topics in Storage and File Systems (pp. 93-99). https://dl.acm.org/doi/10.1145/3538643.3539743
* Im, M., Kang, K., & Yeom, H. (2022, November). Accelerating RocksDB for small-zone ZNS SSDs by parallel I/O mechanism. In Proceedings of the 23rd International Middleware Conference: Industrial Track (pp. 15-21). https://dl.acm.org/doi/abs/10.1145/3564695.3564774
* WA-Zone: Wear-Aware Zone Management Optimization for LSM-Tree on ZNS SSDs (TACO, https://dl.acm.org/doi/abs/10.1145/3637488)
* Persimmon (now accepted at ICCD, https://ieeexplore.ieee.org/abstract/document/10361006)
* LifetimeKV: Narrowing the Lifetime Gap of SSTs in LSMT-based KV Stores for ZNS SSDs (ICCD, https://ieeexplore.ieee.org/abstract/document/10360942)
* FlexZNS: Building High-Performance ZNS SSDs with Size-Flexible and Parity-Protected Zones (ICCD, https://ieeexplore.ieee.org/document/10361036)
* BlzFS: Crash Consistent Log-Structured File System Based on Byte-Loggable Zone for ZNS SSD (ICCD, https://ieeexplore.ieee.org/document/10360948)
* Turn Waste Into Wealth: Alleviating Read/Write Interference in ZNS SSDs: (ICCD, https://ieeexplore.ieee.org/document/10360957)
* Accelerating Flush Operation of LSM Tree by Leveraging the Zone Append Command (ICCE-Asia, https://ieeexplore-ieee-org.vu-nl.idm.oclc.org/abstract/document/10326387)
* SplitZNS: Towards an Efficient LSM-Tree on Zoned Namespace SSDs. ACM Trans. Archit. Code Optim. 20, 3, Article 45 (September 2023), 26 pages. https://doi.org/10.1145/3608476 
* Chen PX., Seo D., Sung C., Park J., Lee M., Li H., Bjørling M., Dutt N. ZoneTrace: A Zone Monitoring Tool for F2FS on ZNS SSDs. ACM Transactions on Design Automation of Electronic Systems. 2024. https://dl.acm.org/doi/abs/10.1145/3656172
* ZMS: Zone Abstraction for Mobile Flash Storage, https://www.usenix.org/system/files/atc24-hwang.pdf 

### 17.2 Other interfaces
  * The Design and Implementation of a Capacity-Variant Storage System, Ziyang Jiao and Xiangqun Zhang, Syracuse University; Hojin Shin and Jongmoo Choi, Dankook University; Bryan S. Kim, Syracuse University, https://www.usenix.org/conference/fast24/presentation/jiao 
  * LightNVM: The Linux Open-Channel SSD Subsystem, https://www.usenix.org/system/files/conference/fast17/fast17-bjorling.pdf
  * "KAML: A Flexible, High-Performance Key-Value SSD," 2017 IEEE International Symposium on High Performance Computer Architecture (HPCA), Austin, TX, USA, 2017, pp. 373-384, doi: 10.1109/HPCA.2017.15. https://ieeexplore.ieee.org/abstract/document/7920840/
  * "Elevating Commodity Storage with the SALSA Host Translation Layer," 2018 IEEE 26th International Symposium on Modeling, Analysis, and Simulation of Computer and Telecommunication Systems (MASCOTS), Milwaukee, WI, USA, 2018, pp. 277-292, doi: 10.1109/MASCOTS.2018.00035. https://ieeexplore.ieee.org/abstract/document/8526893/
  * AutoStream: automatic stream management for multi-streamed SSDs. In Proceedings of the 10th ACM International Systems and Storage Conference (SYSTOR '17). Association for Computing Machinery, New York, NY, USA, Article 3, 1–11. https://doi.org/10.1145/3078468.3078469
  * Jeong-Uk Kang, Jeeseok Hyun, Hyunjoo Maeng, and Sangyeun Cho. 2014. The multi-streamed solid-state drive. In Proceedings of the 6th USENIX conference on Hot Topics in Storage and File Systems (HotStorage'14). USENIX Association, USA, 13.

## 18. SNIA/NVMe weblinks 
  * Storage Trends 2024: Your Questions Answered, https://sniablog.org/storage-trends-your-questions-answered/
  * 2023: FMS-2023-NVM-Express-State-of-the-Union-The-Language-of-Storage.pdf, https://nvmexpress.org/wp-content/uploads/FMS-2023-NVM-Express-State-of-the-Union-The-Language-of-Storage.pdf
  * A Quick Tour of NVM Express (NVMe) https://metebalci.com/blog/a-quick-tour-of-nvm-express-nvme/
  * https://mlcommons.org/working-groups/benchmarks/storage/ MLPerf Storage Working Group
  * 

## 19. Benchmarking, traces, profiling, monitoring, and characterization 
  * LST-Bench: Benchmarking Log-Structured Tables in the Cloud. Proc. ACM Manag. Data 2, 1, Article 59 (February 2024), 26 pages. https://doi.org/10.1145/3639314. 
  * Phitchaya Mangpo Phothilimthana, Saurabh Kadekodi, Soroush Ghodrati, Selene Moon, and Martin Maas. 2024. Thesios: Synthesizing Accurate Counterfactual I/O Traces from I/O Samples. In Proceedings of the 29th ACM International Conference on Architectural Support for Programming Languages and Operating Systems, Volume 3 (ASPLOS '24), Vol. 3. Association for Computing Machinery, New York, NY, USA, 1016–1032. https://doi.org/10.1145/3620666.3651337
  * Jinhong Li, Qiuping Wang, Patrick P. C. Lee, and Chao Shi. 2023. An In-depth Comparative Analysis of Cloud Block Storage Workloads: Findings and Implications. ACM Trans. Storage 19, 2, Article 16 (May 2023), 32 pages. https://doi.org/10.1145/3572779
  * Gala Yadgar, MOSHE Gabel, Shehbaz Jaffer, and Bianca Schroeder. 2021. SSD-based Workload Characteristics and Their Performance Implications. ACM Trans. Storage 17, 1, Article 8 (February 2021), 26 pages. https://doi.org/10.1145/3423137
  * A. K. Paul, O. Faaland, A. Moody, E. Gonsiorowski, K. Mohror and A. R. Butt, "Understanding HPC Application I/O Behavior Using System Level Statistics," 2020 IEEE 27th International Conference on High Performance Computing, Data, and Analytics (HiPC), Pune, India, 2020, pp. 202-211, doi: 10.1109/HiPC50609.2020.00034.
  * S. Kavalanekar, B. Worthington, Qi Zhang and V. Sharda, "Characterization of storage workload traces from production Windows Servers," 2008 IEEE International Symposium on Workload Characterization, Seattle, WA, 2008, pp. 119-128, doi: 10.1109/IISWC.2008.4636097.
  * Tirthak Patel, Suren Byna, Glenn K. Lockwood, and Devesh Tiwari. 2019. Revisiting I/O behavior in large-scale storage systems: the expected and the unexpected. In Proceedings of the International Conference for High Performance Computing, Networking, Storage and Analysis (SC '19). Association for Computing Machinery, New York, NY, USA, Article 65, 1–13. https://doi.org/10.1145/3295500.3356183 
  * Omkar Desai, Seungmin Shin, Eunji Lee, and Bryan S. Kim. 2022. A principled approach for selecting block I/O traces. In Proceedings of the 14th ACM Workshop on Hot Topics in Storage and File Systems (HotStorage '22). Association for Computing Machinery, New York, NY, USA, 52–58. https://doi.org/10.1145/3538643.3539754
  * Large-Scale Analysis of Docker Images and Performance Implications for Container Storage Systems. IEEE Trans. Parallel Distributed Syst. 32(4): 918-930 (2021)
  * Marc-André Vef, Vasily Tarasov, Dean Hildebrand, and André Brinkmann. 2018. Challenges and Solutions for Tracing Storage Systems: A Case Study with Spectrum Scale. ACM Trans. Storage 14, 2, Article 18 (May 2018), 24 pages. https://doi.org/10.1145/3149376 
  * Yang Liu, Raghul Gunasekaran, Xiaosong Ma, and Sudharshan S. Vazhkudai. 2014. Automatic identification of application I/O signatures from noisy server-side traces. In Proceedings of the 12th USENIX conference on File and Storage Technologies (FAST'14). USENIX Association, USA, 213–228.
  * I. Ahmad, "Easy and Efficient Disk I/O Workload Characterization in VMware ESX Server," 2007 IEEE 10th International Symposium on Workload Characterization, Boston, MA, USA, 2007, pp. 149-158, doi: 10.1109/IISWC.2007.4362191.
  * Jayanta Basak, Kushal Wadhwani, and Kaladhar Voruganti. 2016. Storage Workload Identification. ACM Trans. Storage 12, 3, Article 14 (June 2016), 30 pages. https://doi.org/10.1145/2818716
  * Ajay Gulati, Chethan Kumar, and Irfan Ahmad. Storage workload characterization and consolidation in virtualized environments. In Proc. Int'l Workshop on Virtualization Performance: Analysis, Characterization, and Tools (VPACT'09), 2009.
  * Bin Yang, Wei Xue, Tianyu Zhang, Shichao Liu, Xiaosong Ma, Xiyang Wang, and Weiguo Liu. 2023. End-to-end I/O Monitoring on Leading Supercomputers. ACM Trans. Storage 19, 1, Article 3 (February 2023), 35 pages. https://doi.org/10.1145/3568425 (NSDI: https://www.usenix.org/conference/nsdi19/presentation/yang)
  * V. Tarasov, S. Kumar, J. Ma, D. Hildebrand, A. Povzner, G. Kuenning, and E. Zadok. 2012. Extracting flexible, replayable models from large block traces. In Proceedings of the 10th USENIX conference on File and Storage Technologies (FAST'12). USENIX Association, USA, 22. https://static.usenix.org/events/fast12/tech/full_papers/Tarasov.pdf
  * COSBench: cloud object storage benchmark. In Proceedings of the 4th ACM/SPEC International Conference on Performance Engineering (ICPE '13). Association for Computing Machinery, New York, NY, USA, 199–210. https://doi.org/10.1145/2479871.2479900
    
## 20. RAID, Compression, De-duplication 
  * Ziyang Jiao and Bryan S. Kim. 2024. Asymmetric RAID: Rethinking RAID for SSD Heterogeneity. In Proceedings of the 16th ACM Workshop on Hot Topics in Storage and File Systems (HotStorage '24). Association for Computing Machinery, New York, NY, USA, 101–107. https://doi.org/10.1145/3655038.3665952
  * FusionRAID: Achieving Consistent Low Latency for Commodity SSD Arrays, https://www.usenix.org/conference/fast21/presentation/jiang (FAST 2021)
  * StRAID: Stripe-threaded Architecture for Parity-based RAIDs with Ultra-fast SSDs, https://www.usenix.org/conference/atc22/presentation/wang-shucheng (USENIX 2022)
  * Shushu Yi, Yanning Yang, Yunxiao Tang, Zixuan Zhou, Junzhe Li, Chen Yue, Myoungsoo Jung, and Jie Zhang. 2022. ScalaRAID: optimizing linux software RAID system for next-generation storage. In Proceedings of the 14th ACM Workshop on Hot Topics in Storage and File Systems (HotStorage '22). Association for Computing Machinery, New York, NY, USA, 119–125. https://doi.org/10.1145/3538643.3539740
  * 

## 21. ML and (Storage) Systems 
  * R. Macedo et al., "The Case for Storage Optimization Decoupling in Deep Learning Frameworks," 2021 IEEE International Conference on Cluster Computing (CLUSTER), Portland, OR, USA, 2021, pp. 649-656, doi: 10.1109/Cluster48925.2021.00096. https://ieeexplore.ieee.org/document/9556106
  * LLM in a flash: Efficient Large Language Model Inference with Limited Memory, https://arxiv.org/abs/2312.11514.
  * Adding NVMe SSDs to Enable and Accelerate 100B Model Fine-tuning on a Single GPU, https://arxiv.org/pdf/2403.06504 
  * Tectonic-Shift: A Composite Storage Fabric for LargeScale ML Training https://www.usenix.org/system/files/atc23-zhao.pdf 
  * CheckFreq: Frequent, Fine-Grained DNN Checkpointing, https://www.usenix.org/conference/fast21/presentation/mohan
  * Check-N-Run: a Checkpointing System for Training Deep Learning Recommendation Models, https://www.usenix.org/conference/nsdi22/presentation/eisenman
  * Characterization of Large Language Model Development in the Datacenter, https://www.usenix.org/conference/nsdi24/presentation/hu
  * GEMINI: Fast Failure Recovery in Distributed Training with In-Memory Checkpoints. In Proceedings of the 29th Symposium on Operating Systems Principles (SOSP '23). Association for Computing Machinery, New York, NY, USA, 364–381. https://doi.org/10.1145/3600006.3613145
  * Efficient large-scale language model training on GPU clusters using megatron-LM. In Proceedings of the International Conference for High Performance Computing, Networking, Storage and Analysis (SC '21). Association for Computing Machinery, New York, NY, USA, Article 58, 1–15. https://doi.org/10.1145/3458817.3476209
  * PipeDream: generalized pipeline parallelism for DNN training. In Proceedings of the 27th ACM Symposium on Operating Systems Principles (SOSP '19). Association for Computing Machinery, New York, NY, USA, 1–15. https://doi.org/10.1145/3341301.3359646
  * PyTorch distributed: experiences on accelerating data parallel training. Proc. VLDB Endow. 13, 12 (August 2020), 3005–3018. https://doi.org/10.14778/3415478.3415530
  * Analyzing and mitigating data stalls in DNN training. Proc. VLDB Endow. 14, 5 (January 2021), 771–784. https://doi.org/10.14778/3446095.3446100
  * https://proceedings.mlsys.org/ 

## 22. A selection of storage related surveys 
  * 2024 - Survey of vector database management systems. The VLDB Journal 33, 5 (Sep 2024), 1591–1615. https://doi.org/10.1007/s00778-024-00864-x 
  * 2023 -  A Survey on the Integration of NAND Flash Storage in the Design of File Systems and the Host Storage Software Stack, Nick Tehrany, Krijn Doekemeijer, Animesh Trivedi, https://arxiv.org/abs/2307.11866 
  * 2022 - Krijn Doekemeijer, Animesh Trivedi - Key-Value Stores on Flash Storage Devices: A Survey, https://arxiv.org/abs/2205.07975, May 2022.
  * 2023 - Persistent Memory File Systems: A Survey, Wiebe van Breukelen, https://drive.google.com/file/d/1EF-tTEDwYYoFOzywlC-STLqHYlGmyGDx/view
  * 2022 - A Survey of Storage Systems in the RDMA Era, https://dl.acm.org/doi/10.1109/TPDS.2022.3188656.
  * 2022 - Survey of Distributed File System Design Choices, https://dl.acm.org/doi/pdf/10.1145/3465405
  * 2020 - Indexing in flash storage devices: a survey on challenges, current approaches, and future trends. <i>The VLDB Journal</i> 29, 1 (Jan 2020), 273–311. https://doi.org/10.1007/s00778-019-00559-8 https://link.springer.com/content/pdf/10.1007/s00778-019-00559-8.pdf  
  * 2014 - A survey of address translation technologies for flash memories, https://dl.acm.org/doi/10.1145/2512961 
