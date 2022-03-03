---
layout: default
title: Publications
---

You can also browse my <a href="https://scholar.google.com/citations?user=WnQ255cAAAAJ&hl=en" target="_blank">Google Scholar profile</a>.
<br />

#### Conference papers
- <div style="margin-top:20px;">
  [<strong>TPDS</strong>] PostMan: Rapidly Mitigating Bursty Traffic via On-Demand Offloading of Packet Processing.
  Y. Niu, P. Jin, J. Guo, Y Xiao, <strong>R. Shi</strong>, F. Liu, C. Qian, Y. Wang
  In IEEE Transactions on Parallel and Distributed Systems, June 2021
  <span class="links btn-group">
    <a class="btn btn-default btn-xs dropdown-toggle" href="javascript:void(0);" onclick="$('#bib_tpds21').slideToggle('fast');return false;">
      <i class="fa fa-file-code-o"></i> bib
    </a>
    <a class="btn btn-default btn-xs dropdown-toggle" href="javascript:void(0);" onclick="$('#abs_tpds21').slideToggle('fast');return false;">
      <i class="fa fa-file-text-o"></i> abstract
    </a>
    <a class="btn btn-default btn-xs" href="../pub/paper/tpds-2021-rongshi.pdf">
      <i class="fa fa-file-pdf-o"></i> paper
    </a>
    <!--a class="btn btn-default btn-xs" href="">
      <i class="fa fa-file-pdf-o"></i> slides
    </a-->
    <!--a class="btn btn-default btn-xs" href="">
      <i class="fa fa-github-square"></i> code
    </a-->
  </span>
  <div id="bib_tpds21" style="display:none">
    <p style="background-color:#f0f0f0;font-size:70%;">
    @ARTICLE{rong-tpds2021,<br>
    author={Niu, Yipei and Jin, Panpan and Guo, Jian and Xiao, Yikai and Shi, Rong and Liu, Fangming and Qian, Chen and Wang, Yang},<br>
    journal={IEEE Transactions on Parallel and Distributed Systems},<br>
    title={PostMan: Rapidly Mitigating Bursty Traffic via On-Demand Offloading of Packet Processing},<br>
    year={2022},  volume={33},  number={2},  pages={374-387},<br>
    doi={10.1109/TPDS.2021.3092266}
    }
    </p>
  </div>
  <div id="abs_tpds21" class="abstract well" style="display:none">
  <p style="background-color:#f0f0f0;font-size:80%;">
  Unexpected bursty traffic brought by certain sudden events, such as news in the spotlight on a
  social network or discounted items on sale, can cause severe load imbalance in backend services.
  Migrating hot data - the standard approach to achieve load balance - meets a challenge when handling
  such unexpected load imbalance, because migrating data will slow down the server that is already under heavy pressure.
  This article proposes PostMan, an alternative approach to rapidly mitigate load imbalance for services processing small requests.
  Motivated by the observation that processing large packets incurs far less CPU overhead than processing small ones,
  PostMan deploys a number of middleboxes called helpers to assemble small packets into large ones for the heavily-loaded server.
  This approach essentially offloads the overhead of packet processing from the heavily-loaded server to helpers.
  To minimize the overhead, PostMan activates helpers on demand, only when bursty traffic is detected.
  The heavily-loaded server determines when clients connect/disconnect to/from helpers based on the real-time load statistics.
  To tolerate helper failures, PostMan can migrate connections across helpers and can ensure packet ordering despite such migration.
  Driven by real-world workloads, our evaluation shows that, with the help of PostMan, a Memcached server can mitigate bursty
  traffic within hundreds of milliseconds, while migrating data takes tens of seconds and increases the latency during migration. 
  </p>
  </div>
  </div>

- <div style="margin-top:20px;">
  P. Jin, J Guo, Y. Xiao,<strong> R. Shi</strong>, Y. Niu, F. Liu, C. Qian, Y. Wang, PostMan: Rapidly Mitigating Bursty
  Traffic by Offloading Packet Processing, USENIX Annual Technical Conference (<strong>ATC'19</strong>), Renton, USA, 2019
  <span class="links btn-group">
    <a class="btn btn-default btn-xs dropdown-toggle" href="javascript:void(0);" onclick="$('#bib_atc19').slideToggle('fast');return false;">
      <i class="fa fa-file-code-o"></i> bib
    </a>
    <a class="btn btn-default btn-xs dropdown-toggle" href="javascript:void(0);" onclick="$('#abs_atc19').slideToggle('fast');return false;">
      <i class="fa fa-file-text-o"></i> abstract
    </a>
    <a class="btn btn-default btn-xs" href="../pub/paper/atc19-rongshi.pdf">
      <i class="fa fa-file-pdf-o"></i> paper
    </a>
    <a class="btn btn-default btn-xs" href="../pub/slides/atc19-slides.pdf">
      <i class="fa fa-file-pdf-o"></i> slides
    </a>
    <!--a class="btn btn-default btn-xs" href="">
      <i class="fa fa-github-square"></i> code
    </a-->
  </span>
  <div id="bib_atc19" style="display:none">
    <p style="background-color:#f0f0f0;font-size:70%;">
    @inproceedings {rong-atc18,<br>
    author = {Panpan Jin and Jian Guo and Yikai Xiao and Rong Shi and Yipei Niu and Fangming Liu and Chen Qian and Yang Wang},<br>
    title = {PostMan: Rapidly Mitigating Bursty Traffic by Offloading Packet Processing},<br>
    booktitle = {2019 {USENIX} Annual Technical Conference ({USENIX} {ATC} 19)},<br>
    year = {2019},<br>
    address = {Renton, WA},<br>
    pages = {849--862},<br>
    publisher = { {USENIX} Association},<br>
    }
    </p>
  </div>
  <div id="abs_atc19" class="abstract well" style="display:none">
  <p style="background-color:#f0f0f0;font-size:80%;">
  Unexpected bursty traffic due to certain sudden events, such as news
  in the spotlight on a social network or discounted items on sale,
  can cause severe load imbalance in backend services. Migrating hot
  data---the standard approach to achieve load balance---meets a challenge
  when handling such unexpected load imbalance, because migrating data will
  slow down the server that is already under heavy pressure.
  <br>
  This paper proposes PostMan, an alternative approach to rapidly mitigate
  load imbalance for services processing small requests. Motivated by the
  observation that processing large packets incurs far less CPU overhead than
  processing small ones, PostMan deploys a number of middleboxes called helpers
  to assemble small packets into large ones for the heavily-loaded server.
  This approach essentially offloads the overhead of packet processing from
  the heavily-loaded server to others. To minimize the overhead, PostMan
  activates helpers on demand, only when bursty traffic is detected. To
  tolerate helper failures, PostMan can migrate connections across helpers
  and can ensure packet ordering despite such migration. Our evaluation
  shows that, with the help of PostMan, a Memcached server can mitigate
  bursty traffic within hundreds of milliseconds, while migrating data takes
  tens of seconds and increases the latency during migration.
  </p>
  </div>
  </div>


- <div style="margin-top:20px;">
  <strong>R. Shi</strong>, Y. Gan, and Y. Wang, Evaluating Scalability Bottlenecks by Workload Extrapolation,
  IEEE International Symposium on the Modeling, Analysis, and Simulation of Computer and Telecommunication Systems (<strong>MASCOTS'18</strong>),
  Milwaukee, USA, 2018
  <span class="links btn-group">
    <a class="btn btn-default btn-xs dropdown-toggle" href="javascript:void(0);" onclick="$('#bib_mascots18').slideToggle('fast');return false;">
      <i class="fa fa-file-code-o"></i> bib
    </a>
    <a class="btn btn-default btn-xs dropdown-toggle" href="javascript:void(0);" onclick="$('#abs_mascots18').slideToggle('fast');return false;">
      <i class="fa fa-file-text-o"></i> abstract
    </a>
    <a class="btn btn-default btn-xs" href="../pub/paper/mascots2018-rongshi.pdf">
      <i class="fa fa-file-pdf-o"></i> paper
    </a>
    <a class="btn btn-default btn-xs" href="../pub/slides/mascots18-slide.pdf">
      <i class="fa fa-file-pdf-o"></i> slides
    </a>
    <a class="btn btn-default btn-xs" href="https://github.com/OSUSysLab/HadoopMetadataBench">
      <i class="fa fa-github-square"></i> code
    </a>
  </span>
  <div id="bib_mascots18" style="display:none">
    <p style="background-color:#f0f0f0;font-size:70%;">
    @inproceedings{rong-mascots18,<br>
    author = {R. Shi and Y. Gan and Y. Wang},<br>
    booktitle={2018 IEEE 26th International Symposium on Modelling, Analysis and Simulation of Computer and Telecommunication Systems (MASCOTS)},<br>
    title = {Evaluating Scalability Bottlenecks by Workload Extrapolation},<br>
    year = {2018},<br>
    address = {Milwaukee, WI, USA},<br>
    month={Sept},<br>
    }<br>
    </p>
  </div>
  <div id="abs_mascots18" class="abstract well" style="display:none">
  <p style="background-color:#f0f0f0;font-size:80%;">
  Testing a scalability bottleneck requires a large system to generate
  sufficient load, which is usually not accessible to researchers.
  To address this problem, this paper extrapolates the workload to a
  bottleneck node. The key observation that motivates our approach
  is that systems at a large scale are often repeating their behaviors at
  small scales, by running a job more times, running more nodes of the
  same type, or running more iterations of the same loop.
  Following this observation, we record a node’s workloads at
  small scales and extrapolate such workload at a large scale.
  Towards this goal, we have developed PatternMiner, a semi-automatic
  tool to identify how workload patterns change with scale.<br>
  We have tested our method on HDFS NameNode and YARN’s Resource
  Manager. Our evaluation shows that PatternMiner is able to predict
  98% of the workloads for NameNode and 83% of the workloads for the
  Resource Manager. Furthermore, by utilizing the extrapolated workload,
  we are able to emulate a cluster of up to 60,000 nodes with
  only 8 physical machines to evaluate NameNode and Resource Manager.
  </p>
  </div>
  </div>


- <div style="margin-top:20px;">
  <strong>R. Shi</strong>, Y. Wang, Cheap and Available State Machine Replication, USENIX Annual Technical Conference (<strong>ATC'16</strong>),
  Denver, USA, 2016
  <span class="links btn-group">
    <a class="btn btn-default btn-xs dropdown-toggle" href="javascript:void(0);" onclick="$('#bib_atc16').slideToggle('fast');return false;">
      <i class="fa fa-file-code-o"></i> bib
    </a>
    <a class="btn btn-default btn-xs dropdown-toggle" href="javascript:void(0);" onclick="$('#abs_atc16').slideToggle('fast');return false;">
      <i class="fa fa-file-text-o"></i> abstract
    </a>
    <a class="btn btn-default btn-xs" href="https://www.usenix.org/system/files/conference/atc16/atc16_paper-shi.pdf">
      <i class="fa fa-file-pdf-o"></i> paper
    </a>
    <a class="btn btn-default btn-xs" href="../pub/slides/atc16-RongShi.pdf">
      <i class="fa fa-file-pdf-o"></i> slides
    </a>
    <a class="btn btn-default btn-xs" href="https://github.com/vdr007/ThriftyPaxos">
      <i class="fa fa-github-square"></i> code
    </a>
  </span>
  <div id="bib_atc16" style="display:none">
    <p style="background-color:#f0f0f0;font-size:70%;">
    @inproceedings {rong-atc16,<br>
    author = {Rong Shi and Yang Wang},<br>
    title = {Cheap and Available State Machine Replication},<br>
    booktitle = {2016 {USENIX} Annual Technical Conference ({USENIX} {ATC} 16)},<br>
    year = {2016},<br>
    address = {Denver, CO},<br>
    pages = {265--279},<br>
    publisher = { {USENIX} Association},<br>
    <!-- two consecutive "{" error, use "{ {" -->
    }<br>
    </p>
  </div>
  <div id="abs_atc16" class="abstract well" style="display:none">
  <p style="background-color:#f0f0f0;font-size:80%;">
  This paper presents that, by combining on-demand instantiation and lazy
  recovery, we can reduce the cost of asynchronous state machine replication
  protocols, such as Paxos and UpRight, while maintaining their high
  availability. To reduce cost, we incorporate on-demand instantiation,
  which activates a subset of replicas first and activates backup ones when
  active ones fail. To solve its key limitation—the system can be halted
  for long when activating a backup replica, we apply lazy recovery,
  allowing the system to proceed while recovering backup nodes in the
  background. The key contribution of this paper is to identify that,
  when agreement nodes and exe- cution nodes are logically separated,
  they each presents a unique property that enables lazy recovery.
  We have applied this idea to Paxos and built ThriftyPaxos, which,
  as shown in the evaluation, can achieve higher throughput and
  similar availability comparing to standard Paxos,
  despite the fact that ThriftyPaxos activates fewer replicas.
  </p>
  </div>
  </div>

- <div style="margin-top:20px;">
  <strong>R. Shi</strong>, S. Potluri, K. Hamidouche, M. Li, D. Rossetti and D. K. Panda, Designing Efficient Small Message Transfer Mechanism for Inter-node MPI Communication on InfiniBand GPU Clusters, Conference on High Performance Computing (<strong>HiPC'14</strong>), Goa, India, 2014
  <span class="links btn-group">
    <a class="btn btn-default btn-xs dropdown-toggle" href="javascript:void(0);" onclick="$('#bib_hipc14').slideToggle('fast');return false;">
      <i class="fa fa-file-code-o"></i> bib
    </a>
    <a class="btn btn-default btn-xs dropdown-toggle" href="javascript:void(0);" onclick="$('#abs_hipc14').slideToggle('fast');return false;">
      <i class="fa fa-file-text-o"></i> abstract
    </a>
    <a class="btn btn-default btn-xs" href="../pub/paper/rong-hipc14.pdf">
      <i class="fa fa-file-pdf-o"></i> paper
    </a>
    <a class="btn btn-default btn-xs" href="../pub/slides/hipc14-rongshi-slides.pdf">
      <i class="fa fa-file-pdf-o"></i> slides
    </a>
  </span>
  <div id="bib_hipc14" style="display:none">
    <p style="background-color:#f0f0f0;font-size:70%;">
    @INPROCEEDINGS{rong-hipc14,<br>
    author={R. Shi and S. Potluri and K. Hamidouche and J. Perkins and M. Li and D. Rossetti and D. K. Panda},<br>
    booktitle={2014 21st International Conference on High Performance Computing (HiPC)},<br>
    title={Designing efficient small message transfer mechanism for inter-node MPI communication on InfiniBand GPU clusters},<br>
    year={2014},<br>
    pages={1-10},<br>
    address={Goa, India},<br>
    month={Dec},}<br>
    </p>
  </div>
  <div id="abs_hipc14" class="abstract well" style="display:none">
  <p style="background-color:#f0f0f0;font-size:80%;">
  Increasing number of MPI applications are being ported to take advantage of the compute power offered by GPUs. Data movement on GPU clusters continues to be the major bottleneck that keeps scientific applications from fully harnessing the potential of GPUs. Earlier, GPU-GPU inter-node communication has to move data from GPU memory to host memory before sending it over the network. MPI libraries like MVAPICH2 have provided solutions to alleviate this bottleneck using host-based pipelining techniques. Besides that, the newly introduced GPUDirect RDMA (GDR) is a promising solution to further solve this data movement bottleneck. However, existing design in MPI libraries applies the rendezvous protocol for all message sizes, which incurs considerable overhead for small message communications due to extra synchronization message exchange.
  <br>
  In this paper, we propose new techniques to optimize internode GPU-to-GPU communications for small message sizes. Our designs to support the eager protocol include efficient support at both sender and receiver sides. Furthermore, we propose a new data path to provide fast copies between host and GPUs memories. To the best of our knowledge, this is the first study to propose efficient designs for GPU communication for small message sizes, using eager protocol. Our experimental results demonstrate up to 45% and 63% reduction in latency for GPU-to-GPU and CPU-to-GPU point-to-piont communications, respectively. These designs boost the uni-directional bandwidth by 7.3x and 1.7x, respectively. We also evaluate our proposed design with two end-applications: GPULBM and HOOMD-blue. Performance numbers on Kepler GPUs shows that, compared to the best existing GDR design, our proposed designs achieve up to 23.4% latency reduction for GPULBM and 20.1% increase in average TPS for HOOMDblue, respectively.
  </p>
  </div>
  </div>


- <div style="margin-top:20px;">
  J. Zhang, X. Lu, J. Jose, M. Li, <strong>R. Shi</strong> and D. K. Panda, High Performance MPI Library over SR-IOV Enabled InfiniBand Clusters, Conference on High Performance Computing (<strong>HiPC'14</strong>), Goa, India, 2014
  <span class="links btn-group">
    <a class="btn btn-default btn-xs dropdown-toggle" href="javascript:void(0);" onclick="$('#bib_hipc14_2').slideToggle('fast');return false;">
      <i class="fa fa-file-code-o"></i> bib
    </a>
    <a class="btn btn-default btn-xs dropdown-toggle" href="javascript:void(0);" onclick="$('#abs_hipc14_2').slideToggle('fast');return false;">
      <i class="fa fa-file-text-o"></i> abstract
    </a>
    <a class="btn btn-default btn-xs" href="../pub/paper/zhang-hipc14.pdf">
      <i class="fa fa-file-pdf-o"></i> paper
    </a>
  </span>
  <div id="bib_hipc14_2" style="display:none">
    <p style="background-color:#f0f0f0;font-size:70%;">
    @InProceedings{jie-hipc14,<br>
      author =       {J. Zhang, X. Lu, J. Jose, M. Li, R. Shi, D. K. Panda},<br>
      title =        {High Performance MPI Library over SR-IOV Enabled InfiniBand Clusters},<br>
      booktitle =    {Proceedings of International Conference on High Performance Computing (HiPC)},<br>
      year =         2014,<br>
      address =      {Goa, India},<br>
      month =        {December 17-20}<br>
    }<br>
    </p>
  </div>
  <div id="abs_hipc14_2" class="abstract well" style="display:none">
  <p style="background-color:#f0f0f0;font-size:80%;">
  Virtualization has become a central role in HPC Cloud due to easy management and low cost of computation and communication. Recently, Single Root I/O Virtualization (SR-IOV) technology has been introduced for high-performance interconnects such as InfiniBand and can attain near to native performance for inter-node communication. However, the SR-IOV scheme lacks locality aware communication support, which leads to performance overheads for inter-VM communication within a same physical node. To address this issue, this paper first proposes a high performance design of MPI library over SR-IOV enabled InfiniBand clusters by dynamically detecting VM locality and coordinating data movements between SR-IOV and Inter-VM shared memory (IVShmem) channels. Through our proposed design, MPI applications running in virtualized mode can achieve efficient locality-aware communication on SR-IOV enabled InfiniBand clusters. In addition, we optimize communications in IVShmem and SR-IOV channels by analyzing the performance impact of core mechanisms and parameters inside MPI library to deliver better performance in virtual machines. Finally, we conduct comprehensive performance studies by using point-to-point and collective benchmarks, and HPC applications. Experimental evaluations show that our proposed MPI library design can significantly improve the performance for point-to-point and collective operations, and MPI applications with different InfiniBand transport protocols (RC and UD) by up to 158%, 76%, 43%, respectively, compared with SR-IOV. To the best of our knowledge, this is the first study to offer a high performance MPI library that supports efficient locality aware MPI communication over SR-IOV enabled InfiniBand clusters.
  </p>
  </div>
  </div>

- <div style="margin-top:20px;">
  J. Zhang, X. Lu, J. Jose, <strong>R. Shi</strong> and D. K. Panda, Can Inter-VM Shmem Benefit MPI Applications on SR-IOV based Virtualized InfiniBand Clusters, European Conference on Parallel Processing (<strong>Euro-Par'14</strong>), Porto, Portugal, 2014
  <span class="links btn-group">
    <a class="btn btn-default btn-xs dropdown-toggle" href="javascript:void(0);" onclick="$('#bib_europar14').slideToggle('fast');return false;">
      <i class="fa fa-file-code-o"></i> bib
    </a>
    <a class="btn btn-default btn-xs dropdown-toggle" href="javascript:void(0);" onclick="$('#abs_europar14').slideToggle('fast');return false;">
      <i class="fa fa-file-text-o"></i> abstract
    </a>
    <a class="btn btn-default btn-xs" href="../pub/paper/zhang-europar14.pdf">
      <i class="fa fa-file-pdf-o"></i> paper
    </a>
  </span>
  <div id="bib_europar14" style="display:none">
    <p style="background-color:#f0f0f0;font-size:70%;">
    @InProceedings{jie-europar14,<br>
      author =       {J. Zhang, X. Lu, J. Jose, R. Shi, D. K. Panda},<br>
      title =        {Can Inter-VM Shmem Benefit MPI Applications on
                        SR-IOV based Virtualized InfiniBand Clusters?},<br>
      booktitle =    {Proceedings of 20th International Conference Euro-Par 2014
                      Parallel Processing},<br>
      year =         2014,<br>
      address =      {Porto, Portugal},<br>
      month =        {August 25-29}<br>
    }<br>
    </p>
  </div>
  <div id="abs_europar14" class="abstract well" style="display:none">
  <p style="background-color:#f0f0f0;font-size:80%;">
  Single Root I/O Virtualization (SR-IOV) technology has been introduced for high-performance interconnects such as InfiniBand. Recent studies mainly focus on performance characteristics of high-performance communication middleware (e.g. MPI) and applications on SR-IOV enabled HPC clusters. However, current SR-IOV based MPI applications do not take advantage of the locality-aware communication on intra-host inter-VM environment. Although Inter-VM Shared Memory (IVShmem) has been proven to support efficient locality-aware communication, the performance benefits of IVShmem for MPI libraries on virtualized environments are yet to be explored. In this paper, we present a comprehensive performance evaluation for IVShmem backed MPI using micro-benchmarks and HPC applications. The performance evaluations show that, through IVShmem, the performance of MPI point-to-point and collective operations can be improved up to 193% and 91%, respectively. The application performance can be improved up to 96%, compared to SR-IOV. The results further show that IVShmem just brings minor overhead compared to native environment.
  </p>
  </div>
  </div>

- <div style="margin-top:20px;">
  <strong>R. Shi</strong>, X. Lu, S. Potluri, K. Hamidouche, J. Zhang, and D. K. Panda, HAND: A Hybrid Approach to Accelerate Non-contiguous Data Movement using MPI Datatypes on GPU Clusters, in Proceeding of International Conference on Parallel Processing (<strong>ICPP'14</strong>), Minneapolis, USA, 2014
  <span class="links btn-group">
    <a class="btn btn-default btn-xs dropdown-toggle" href="javascript:void(0);" onclick="$('#bib_icpp14').slideToggle('fast');return false;">
      <i class="fa fa-file-code-o"></i> bib
    </a>
    <a class="btn btn-default btn-xs dropdown-toggle" href="javascript:void(0);" onclick="$('#abs_icpp14').slideToggle('fast');return false;">
      <i class="fa fa-file-text-o"></i> abstract
    </a>
    <a class="btn btn-default btn-xs" href="../pub/paper/rong-icpp14.pdf">
      <i class="fa fa-file-pdf-o"></i> paper
    </a>
    <a class="btn btn-default btn-xs" href="../pub/slides/icpp14-rongshi-slides.pdf">
      <i class="fa fa-file-pdf-o"></i> slides
    </a>
  </span>
  <div id="bib_icpp14" style="display:none">
    <p style="background-color:#f0f0f0;font-size:70%;">
    @INPROCEEDINGS{rong-icpp14,<br>
    author={R. Shi and X. Lu and S. Potluri and K. Hamidouche and J. Zhang and D. K. Panda},<br>
    booktitle={2014 43rd International Conference on Parallel Processing},<br>
    title={HAND: A Hybrid Approach to Accelerate Non-contiguous Data Movement Using MPI Datatypes on GPU Clusters},<br>
    year={2014},<br>
    pages={221-230},<br>
    address = {Minneapolis, MN, USA},<br>
    month={Sept},}<br>
    </p>
  </div>
  <div id="abs_icpp14" class="abstract well" style="display:none">
  <p style="background-color:#f0f0f0;font-size:80%;">
  Increasing number of MPI applications are being ported to take advantage of the compute power offered by GPUs. Data movement continues to be the major bottleneck on GPU clusters, more so when data is non-contiguous, which is a common case in scientific applications. Existing techniques to optimize MPI datatype processing to improve performance of non-contiguous data movement handle only certain data patterns efficiently while incurring overheads for the others. In this paper, we first propose a set of optimized techniques to handle different MPI datatypes. Next, we propose a novel framework (HAND) that enables hybrid and adaptive selection among different techniques and tuning to achieve better performance with all datatypes. Our experimental results using modified DDTBench suite demonstrate up to 98% reduction in datatype latency. We also apply datatype aware design on an N-Body particle simulation application. Performance evaluation of this application on a 64 GPU cluster shows that our proposed approach can achieve up to 80% and 54% increase in performance by using struct and indexed datatypes compared to the existing best design. To the best of our knowledge, this is the first attempt to propose a hybrid and adaptive solution to integrate all existing schemes to optimize arbitrary non-contiguous data movement using MPI datatypes on GPU clusters.
  </p>
  </div>
  </div>

- <div style="margin-top:20px;">
  <strong>R. Shi</strong>, S. Potluri, K. Hamidouche, X. Lu, K. Tomko and D. K. Panda, A Scalable and Portable Approach to Accelerate Hybrid HPL on 
Heterogeneous CPU-GPU Clusters, IEEE International Conference on Cluster Computing (<strong>Cluster'13</strong>), Indianapolis, USA, 2013, <font color="red"><strong>Best Student Paper Award</strong></font>
  <span class="links btn-group">
    <a class="btn btn-default btn-xs dropdown-toggle" href="javascript:void(0);" onclick="$('#bib_cluster13').slideToggle('fast');return false;">
      <i class="fa fa-file-code-o"></i> bib
    </a>
    <a class="btn btn-default btn-xs dropdown-toggle" href="javascript:void(0);" onclick="$('#abs_cluster13').slideToggle('fast');return false;">
      <i class="fa fa-file-text-o"></i> abstract
    </a>
    <a class="btn btn-default btn-xs" href="../pub/paper/rong-cluster13.pdf">
      <i class="fa fa-file-pdf-o"></i> paper
    </a>
    <a class="btn btn-default btn-xs" href="../pub/slides/Cluster13-rongshi-slides.pdf">
      <i class="fa fa-file-pdf-o"></i> slides
    </a>
  </span>
  <div id="bib_cluster13" style="display:none">
    <p style="background-color:#f0f0f0;font-size:70%;">
    @INPROCEEDINGS{rong-cluster13,<br>
    author={R. Shi and S. Potluri and K. Hamidouche and X. Lu and K. Tomko and D. K. Panda},<br>
    booktitle={2013 IEEE International Conference on Cluster Computing (CLUSTER)},<br>
    title={A scalable and portable approach to accelerate hybrid HPL on heterogeneous CPU-GPU clusters},<br>
    year={2013},<br>
    pages={1-8},<br>
    address = {Indianapolis, IN, USA},<br>
    month={Sept},}<br>
    </p>
  </div>
  <div id="abs_cluster13" class="abstract well" style="display:none">
  <p style="background-color:#f0f0f0;font-size:80%;">
  Accelerating High-Performance Linkpack (HPL) on heterogeneous clusters with multi-core CPUs and GPUs has attracted a lot of attention from the High Performance Computing community. It is becoming common for large scale clusters to have GPUs on only a subset of nodes in order to limit system costs. The major challenge for HPL in this case is to efficiently take advantage of all the CPU and GPU resources available on a cluster. In this paper, we present a novel two-level workload partitioning approach for HPL that distributes workload based on the compute power of CPU/GPU nodes across the cluster. Our approach also handles multi-GPU configurations. Unlike earlier approaches for heterogeneous clusters with CPU and GPU nodes, our design takes advantage of asynchronous kernel launches and CUDA copies to overlap computation and CPU-GPU data movement. It uses techniques such as process grid reordering to reduce MPI communication/contention while ensuring load balance across nodes. Our experimental results using 32 GPU and 128 CPU nodes of Oakley, a research cluster at Ohio Supercomputer Center, shows that our proposed approach can achieve more than 80% of combined actual peak performance of CPU and GPU nodes. This provides 47% and 63% increase in the HPL performance that can be reported using only CPU nodes and only GPU nodes, respectively.
  </p>
  </div>
  </div>

<br />
