## Welcome to the VU Amsterdam - storage-systems wiki!
We will collect and grow the reading list for the Storage Systems class (https://animeshtrivedi.github.io/course-stosys/) at VU Amsterdam. ***All lecture slides are publically available.***

Hands-on wiki with commands and setup is available here: https://github.com/animeshtrivedi/storage-systems-wiki-reading-list/wiki

We are also collecting nice surveys we can find: https://github.com/stonet-research/storage-systems-wiki-reading-list#a-selection-of-storage-related-surveys 

**Contributions:** please open a pull request with 1-2 line description of the paper! 

## Reading list 

### NVM storage and device-level details 
  * Improving Flash Storage Performance by Caching Address Mapping Table in Host Memory, https://www.usenix.org/conference/hotstorage17/program/presentation/jeong
  * 


### Flash FTL designs, patterns, and GC designs 
  * 

### Host interfacing, OS and Storage I/O Stack  
  * Theano Stavrinos, Daniel S. Berger, Ethan Katz-Bassett, and Wyatt Lloyd. 2021. Don't be a blockhead: zoned namespaces make work on conventional SSDs obsolete. In Proceedings of the Workshop on Hot Topics in Operating Systems (HotOS '21). Association for Computing Machinery, New York, NY, USA, 144–151. https://doi.org/10.1145/3458336.3465300
     * ZNS is the new and exciting interface for NVM storage. It is also quite fundamental as the paper argues that it solves or makes old problems with flash useless. A good fun read (plus, summarizes a decade worth of research effort in managing flash)  
  * FlatFlash: Exploiting the Byte-Accessibility of SSDs within a Unified Memory-Storage Hierarchy, ASPLOS 2019, https://dl-acm-org.vu-nl.idm.oclc.org/doi/abs/10.1145/3297858.3304061  * 

### Flash I/O Scheduling and quality-of-service/multi-tenancy 
  * BlockFlex: Enabling Storage Harvesting with Software-Defined Flash in Modern Cloud Platforms, OSDI 2022. https://www.usenix.org/conference/osdi22/presentation/reidys 
  * FLIN: https://ieeexplore.ieee.org/abstract/document/8416843
  * D2FQ: https://www.usenix.org/system/files/fast21-woo.pdf
  * blk-switch: https://www.usenix.org/system/files/osdi21-hwang.pdf
  * I/O Schedulers for Proportionality and Stability on Flash-Based SSDs in Multi-Tenant Environments
  * FastResponse: https://dl.acm.org/doi/pdf/10.1145/3524059.3532378

### File Systems 
  * 

### Key-Value Storage 
  * Stratos Idreos and Mark Callaghan. 2020. Key-Value Storage Engines. In Proceedings of the 2020 ACM SIGMOD International Conference on Management of Data (SIGMOD '20). Association for Computing Machinery, New York, NY, USA, 2667–2672. https://doi.org/10.1145/3318464.3383133 
     * A small write up summarizing (2020) the current popular indexing structures about KV data structures 
  * Designing Access Methods: The RUM Conjecture (Read, Update, and Memory): https://stratos.seas.harvard.edu/files/stratos/files/rum.pdf
     * A good fundamental work that discusses that a single data structure cannot provide most optimal performance for all three types of operations
  * https://www.vldb.org/pvldb/vol14/p2216-sarkar.pdf, Constructing and Analyzing the LSM Compaction Design Space
  * DComp: Efficient Offload of LSM-tree Compaction with Data Processing Units, https://dl.acm.org/doi/abs/10.1145/3605573.3605633 


### Storage Virtualization 
  *  MDev-NVMe (mediated passthrough): https://www.usenix.org/system/files/conference/atc18/atc18-peng.pdf
  *  Analyzing, modeling, and provisioning QoS for NVMe ssds: https://ieeexplore.ieee.org/abstract/document/8603171/
  *  Spdk vhost-nvme (user-space): Accelerating i/os in virtual machines on nvme ssds via user space vhost target: https://ieeexplore.ieee.org/abstract/document/8567374/
  *  FlashBlox: https://www.usenix.org/system/files/conference/fast17/fast17_huang.pdf

### Storage emulation/simulation
* MQsim (simulator): https://www.usenix.org/system/files/conference/fast18/fast18-tavakkol.pdf
* FEMU (emulator): https://www.usenix.org/system/files/conference/fast18/fast18-li.pdf
* NVMeVirt (emulator): https://www.usenix.org/conference/fast23/presentation/kim-sang-hoon
* Amber https://ieeexplore.ieee.org/abstract/document/8574562  and for ZNS: https://ieeexplore.ieee.org/abstract/document/996440
* Wear distributions in FF-SSD: https://dl.acm.org/doi/abs/10.1145/3538643.3539757 
* Nameless writes had an emulator. How does it work? https://www.usenix.org/legacy/event/fast12/tech/full_papers/Zhang2-7-12.pdf 
* Goliath allows evaluating large (1TB at that time) workloads on small disks without performance gaps.

### Reliability and failures studies  
  * 

### Programmable storage, acceleration, offloading, computational storage, workload-specific storage   
  * Kiran Kumar Matam, Gunjae Koo, Haipeng Zha, Hung-Wei Tseng, and Murali Annavaram. 2019. GraphSSD: graph semantics aware SSD. In Proceedings of the 46th International Symposium on Computer Architecture (ISCA '19). Association for Computing Machinery, New York, NY, USA, 116–128. https://doi.org/10.1145/3307650.3322275
  * Yunjae Lee, Jinha Chung, and Minsoo Rhu. 2022. SmartSAGE: training large-scale graph neural networks using in-storage processing architectures. In Proceedings of the 49th Annual International Symposium on Computer Architecture (ISCA '22). Association for Computing Machinery, New York, NY, USA, 932–945. https://doi.org/10.1145/3470496.3527391
  * Hongsu Byun, Safdar Jamil, Jungwook Han, Sungyong Park, Myungcheol Lee, Changsoo Kim, Beongjun Choi, and Youngjae Kim. 2023. An Analytical Model-based Capacity Planning Approach for Building CSD-based Storage Systems. ACM Trans. Embed. Comput. Syst. Just Accepted (September 2023). https://doi.org/10.1145/3623677
  * Juno Kim and Steven Swanson. 2022. Blaze: fast graph processing on fast SSDs. In Proceedings of the International Conference on High Performance Computing, Networking, Storage and Analysis (SC '22). IEEE Press, Article 44, 1–15. (Github: https://github.com/NVSL/blaze ) 
  * X. Liao et al., "A Structure-Aware Storage Optimization for Out-of-Core Concurrent Graph Processing," in IEEE Transactions on Computers, vol. 71, no. 7, pp. 1612-1625, 1 July 2022, doi: 10.1109/TC.2021.3098976.
  * X. Xu, F. Wang, H. Jiang, Y. Cheng, D. Feng and Y. Zhang, "A Hybrid Update Strategy for I/O-Efficient Out-of-Core Graph Processing," in IEEE Transactions on Parallel and Distributed Systems, vol. 31, no. 8, pp. 1767-1782, 1 Aug. 2020, doi: 10.1109/TPDS.2020.2973143.
  * GraphWalker: An I/O-Efficient and Resource-Friendly Graph Analytic System for Fast and Scalable Random Walks, https://www.usenix.org/conference/atc20/presentation/wang-rui
  * Chun-Yi Liu, Wonil Choi, Soheil Khadirsharbiyani, and Mahmut Kandemir. 2023. MBFGraph: An SSD-based External Graph System for Evolving Graphs. In Proceedings of the International Conference for High Performance Computing, Networking, Storage and Analysis (SC '23). Association for Computing Machinery, New York, NY, USA, Article 24, 1–13. https://doi.org/10.1145/3581784.3607070
  * Sang-Woo Jun, Andy Wright, Sizhuo Zhang, Shuotao Xu, and Arvind. 2018. GraFboost: using accelerated flash storage for external graph analytics. In Proceedings of the 45th Annual International Symposium on Computer Architecture (ISCA '18). IEEE Press, 411–424. https://doi.org/10.1109/ISCA.2018.00042
  * GLIST: Towards In-Storage Graph Learning, https://www.usenix.org/conference/atc21/presentation/li-cangyuan
  * Hardware/Software Co-Programmable Framework for Computational SSDs to Accelerate Deep Learning Service on Large-Scale Graphs, https://www.usenix.org/conference/fast22/presentation/kwon
  * GraFboost: using accelerated flash storage for external graph analytics. In Proceedings of the 45th Annual International Symposium on Computer Architecture (ISCA '18). IEEE Press, 411–424. https://doi.org/10.1109/ISCA.2018.00042
  * Lambda-IO: A Unified IO Stack for Computational Storage, https://www.usenix.org/system/files/fast23-yang-zhe.pdf  
  * https://people.csail.mit.edu/jshun/graph.shtml
  * 
### Performance (mostly with OS/APIs) 
  * Diego Didona, Jonas Pfefferle, Nikolas Ioannou, Bernard Metzler, and Animesh Trivedi. 2022. Understanding modern storage APIs: a systematic study of libaio, SPDK, and io_uring. In Proceedings of the 15th ACM International Conference on Systems and Storage (SYSTOR '22). Association for Computing Machinery, New York, NY, USA, 120–127. https://doi.org/10.1145/3534056.3534945
  * Gabriel Haas and Viktor Leis. 2023. What Modern NVMe Storage Can Do, and How to Exploit it: High-Performance I/O for High-Performance Storage Engines. Proc. VLDB Endow. 16, 9 (May 2023), 2090–2102. https://doi.org/10.14778/3598581.3598584
  * Zebin Ren and Animesh Trivedi. 2023. Performance Characterization of Modern Storage Stacks: POSIX I/O, libaio, SPDK, and io_uring. In Proceedings of the 3rd Workshop on Challenges and Opportunities of Efficient and Performant Storage Systems (CHEOPS '23). Association for Computing Machinery, New York, NY, USA, 35–45. https://doi.org/10.1145/3578353.3589545
  * 

### Persistent Memories / disaggregation / CXL 
  * Hasan Al Maruf, Hao Wang, Abhishek Dhanotia, Johannes Weiner, Niket Agarwal, Pallab Bhattacharya, Chris Petersen, Mosharaf Chowdhury, Shobhit Kanaujia, and Prakash Chauhan. 2023. TPP: Transparent Page Placement for CXL-Enabled Tiered-Memory. In Proceedings of the 28th ACM International Conference on Architectural Support for Programming Languages and Operating Systems, Volume 3 (ASPLOS 2023). Association for Computing Machinery, New York, NY, USA, 742–755. https://doi.org/10.1145/3582016.3582063 
  * Huaicheng Li, Daniel S. Berger, Lisa Hsu, Daniel Ernst, Pantea Zardoshti, Stanko Novakovic, Monish Shah, Samir Rajadnya, Scott Lee, Ishwar Agarwal, Mark D. Hill, Marcus Fontoura, and Ricardo Bianchini. 2023. Pond: CXL-Based Memory Pooling Systems for Cloud Platforms. In Proceedings of the 28th ACM International Conference on Architectural Support for Programming Languages and Operating Systems, Volume 2 (ASPLOS 2023). Association for Computing Machinery, New York, NY, USA, 574–587. https://doi.org/10.1145/3575693.3578835 
  * Miryeong Kwon, Sangwon Lee, and Myoungsoo Jung. 2023. Cache in Hand: Expander-Driven CXL Prefetcher for Next Generation CXL-SSD. In Proceedings of the 15th ACM Workshop on Hot Topics in Storage and File Systems (HotStorage '23). Association for Computing Machinery, New York, NY, USA, 24–30. https://doi.org/10.1145/3599691.3603406 
  * Myoungsoo Jung. 2022. Hello bytes, bye blocks: PCIe storage meets compute express link for memory expansion (CXL-SSD). In Proceedings of the 14th ACM Workshop on Hot Topics in Storage and File Systems (HotStorage '22). Association for Computing Machinery, New York, NY, USA, 45–51. https://doi.org/10.1145/3538643.3539745 
  * Jianguo Wang and Qizhen Zhang. 2023. Disaggregated Database Systems. In Companion of the 2023 International Conference on Management of Data (SIGMOD '23). Association for Computing Machinery, New York, NY, USA, 37–44. https://doi.org/10.1145/3555041.3589403 
  * Hasan Al Maruf and Mosharaf Chowdhury. 2023. Memory Disaggregation: Advances and Open Challenges. SIGOPS Oper. Syst. Rev. 57, 1 (June 2023), 29–37. https://doi.org/10.1145/3606557.3606562 
  * Marcos K. Aguilera, Emmanuel Amaro, Nadav Amit, Erika Hunhoff, Anil Yelam, and Gerd Zellweger. 2023. Memory disaggregation: why now and what are the challenges. SIGOPS Oper. Syst. Rev. 57, 1 (June 2023), 38–46. https://doi.org/10.1145/3606557.3606563
  * Direct Access, High-Performance Memory Disaggregation with DirectCXL, https://www.usenix.org/conference/atc22/presentation/gouk
  * FlatFS: Flatten Hierarchical File System Namespace on Non-volatile Memories, https://www.usenix.org/conference/atc22/presentation/cai 
  * Poseidon: Safe, Fast and Scalable Persistent Memory Allocator (Middleware, 2020), https://dl.acm.org/doi/10.1145/3423211.3425671 
  * Persistent State Machines for Recoverable In-memory Storage Systems with NVRam,  https://www.usenix.org/conference/osdi20/presentation/zhang-wen

### Networked/distributed Flash 
  * RackBlox: A Software-Defined Rack-Scale Storage System with Network-Storage Co-Design, https://dl.acm.org/doi/10.1145/3600006.3613170

### Distributed/Cloud/Operating systems 
  * Reducing Minor Page Fault Overheads through Enhanced Page Walker, https://dl.acm.org/doi/full/10.1145/3547142 

### NVM storage and Energy consumption 
  * Bryan Harris and Nihat Altiparmak. When poll is more energy efficient than interrupt. In Proceedings of the 14th ACM Workshop on Hot Topics in Storage and File Systems, HotStorage ’22, page 59–64, New York, NY, USA, 2022. Association for Computing Machinery.  https://www.hotstorage.org/2022/slides/hotstorage22-paper44-presentation_slides.pdf
  * Bryan Harris and Nihat Altiparmak. Ultra‐low latency ssds’ impact on overall energy efficiency. In Proceedings of the 12th USENIX Conference on Hot Topics in Storage and File Systems, HotStorage’20, USA, 2020. USENIX Association. https://www.usenix.org/system/files/hotstorage20-paper61-slides-harris.pdf
  * Jing Li, Anirudh Badam, Ranveer Chandra, Steven Swanson, Bruce Worthington, and Qi Zhang. On the energy overhead of mobile storage systems. In Proceedings of the 12th USENIX Conference on File and Storage Technologies, FAST’14, page 105–118, USA, 2014. USENIX Association.
  * Jayashree Mohan, Dhathri Purohith, Mathew Halpern, Vijay Chidambaram, and Vijay Janapa Reddi. Storage on your smartphone uses more energy than you think. In Proceedings of the 9th USENIX Conference on Hot Topics in Storage and File Systems, HotStorage’17, page 9, USA, 2017. USENIX Association.
  * Kargar, Saeed and Nawab, Faisal. Hamming Tree: The Case for Energy-Aware Indexing for NVMs. In Proceedings of the ACM on Management of Data. SIGMOD'2023. ACM New York, NY, USA, 2023. 

### Timeseries databases
  * Jalal Mostafa, Sara Wehbi, Suren Chilingaryan, Andreas Kopmann. 2022. SciTS: A Benchmark for Time-Series Databases in Scientific Experiments and Industrial Internet of Things. https://arxiv.org/abs/2204.09795v2
      * Paper describing a system for benchmarking the performance of timeseries databases. The paper generates data used to benchmark the performance of insertion and uses a few queries to test the performance of the querying engines.

### New systems architectures 
  * FpgaNIC: An FPGA-based Versatile 100Gb SmartNIC for GPUs https://www.usenix.org/system/files/atc22-wang-zeke.pdf 

### New flash storage interfaces

#### ZNS: Explanations, research directions and ZNS extensions
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

#### ZNS: Specific applications/software modified for ZNS
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


#### Other interfaces
* OCSSD: https://www.usenix.org/system/files/conference/fast17/fast17-bjorling.pdf
* KV-SSDs: https://ieeexplore.ieee.org/abstract/document/7920840/
* SALSA (FTL to host): https://ieeexplore.ieee.org/abstract/document/8526893/

### SNIA/NVMe weblinks 
  * 2023: FMS-2023-NVM-Express-State-of-the-Union-The-Language-of-Storage.pdf, https://nvmexpress.org/wp-content/uploads/FMS-2023-NVM-Express-State-of-the-Union-The-Language-of-Storage.pdf

### Traces, profiling, monitoring, and characterization 
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
    
### RAID, Compression, De-duplication 
  * FusionRAID: Achieving Consistent Low Latency for Commodity SSD Arrays, https://www.usenix.org/conference/fast21/presentation/jiang (FAST 2021)
  * StRAID: Stripe-threaded Architecture for Parity-based RAIDs with Ultra-fast SSDs, https://www.usenix.org/conference/atc22/presentation/wang-shucheng (USENIX 2022)
  * Shushu Yi, Yanning Yang, Yunxiao Tang, Zixuan Zhou, Junzhe Li, Chen Yue, Myoungsoo Jung, and Jie Zhang. 2022. ScalaRAID: optimizing linux software RAID system for next-generation storage. In Proceedings of the 14th ACM Workshop on Hot Topics in Storage and File Systems (HotStorage '22). Association for Computing Machinery, New York, NY, USA, 119–125. https://doi.org/10.1145/3538643.3539740
  * 


### A selection of storage related surveys 
[2023] 
  * A Survey on the Integration of NAND Flash Storage in the Design of File Systems and the Host Storage Software Stack, Nick Tehrany, Krijn Doekemeijer, Animesh Trivedi, https://arxiv.org/abs/2307.11866 

[2022]
  * Krijn Doekemeijer, Animesh Trivedi - Key-Value Stores on Flash Storage Devices: A Survey, https://arxiv.org/abs/2205.07975, May 2022.
  * Persistent Memory File Systems: A Survey, Wiebe van Breukelen, https://drive.google.com/file/d/1EF-tTEDwYYoFOzywlC-STLqHYlGmyGDx/view
  * http://madsys.cs.tsinghua.edu.cn/publications/TPDS2022-ma.pdf, a Survey of Storage Systems in the RDMA Era.
  * Survey of Distributed File System Design Choices, https://dl.acm.org/doi/pdf/10.1145/3465405

[prior] 
  * Athanasios Fevgas, Leonidas Akritidis, Panayiotis Bozanis, and Yannis Manolopoulos. 2020. Indexing in flash storage devices: a survey on challenges, current approaches, and future trends. <i>The VLDB Journal</i> 29, 1 (Jan 2020), 273–311. https://doi.org/10.1007/s00778-019-00559-8 https://link.springer.com/content/pdf/10.1007/s00778-019-00559-8.pdf  
     * One of the most comprehensive and well-written surveys on indexing data structures on flash storage 

  
