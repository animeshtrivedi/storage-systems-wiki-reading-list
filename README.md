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

### Programmable storage, acceleration, offloading, computational storage  
  * 

### Persistent Memories 
  * Direct Access, High-Performance Memory Disaggregation with DirectCXL, https://www.usenix.org/conference/atc22/presentation/gouk
  * FlatFS: Flatten Hierarchical File System Namespace on Non-volatile Memories, https://www.usenix.org/conference/atc22/presentation/cai 
  * Poseidon: Safe, Fast and Scalable Persistent Memory Allocator (Middleware, 2020), https://dl.acm.org/doi/10.1145/3423211.3425671 
  * Persistent State Machines for Recoverable In-memory Storage Systems with NVRam,  https://www.usenix.org/conference/osdi20/presentation/zhang-wen

### Networked/distributed Flash 
  * 

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

#### Other interfaces
* OCSSD: https://www.usenix.org/system/files/conference/fast17/fast17-bjorling.pdf
* KV-SSDs: https://ieeexplore.ieee.org/abstract/document/7920840/
* SALSA (FTL to host): https://ieeexplore.ieee.org/abstract/document/8526893/

### A selection of storage related surveys 
  * Krijn Doekemeijer, Animesh Trivedi - Key-Value Stores on Flash Storage Devices: A Survey, https://arxiv.org/abs/2205.07975, May 2022.   
  * Athanasios Fevgas, Leonidas Akritidis, Panayiotis Bozanis, and Yannis Manolopoulos. 2020. Indexing in flash storage devices: a survey on challenges, current approaches, and future trends. <i>The VLDB Journal</i> 29, 1 (Jan 2020), 273–311. https://doi.org/10.1007/s00778-019-00559-8 https://link.springer.com/content/pdf/10.1007/s00778-019-00559-8.pdf  
     * One of the most comprehensive and well-written surveys on indexing data structures on flash storage 
  * http://madsys.cs.tsinghua.edu.cn/publications/TPDS2022-ma.pdf, a Survey of Storage Systems in the RDMA Era. 
  * Survey of Distributed File System Design Choices, https://dl.acm.org/doi/pdf/10.1145/3465405
