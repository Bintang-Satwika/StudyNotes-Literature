# Towards Energy Efficient 5G Networks Using Machine Learning: Taxonomy, Research Challenges, and Future Research Directions 

## ABOUT

| item | information |
| --- | --- |
| Paper Link |https://ieeexplore.ieee.org/document/9218920|
| Authors | Mohammad Tahir,  Amna Mughees , etc.|
| Date of Publication |  09 October 2020 |
|type |Journals & Magazines : IEEE Access|
| total pages |  24 pages (187498 - 187522) |
| keywords | 5G, energy effciency, millimeter wave, machine learning, massive MIMO, SDN, NFV,CRAN, HetNet.|

The paper aims to provide a comprehensive survey on  addressing energy effciency in 5G network challenges  encountered in enabling technologies such as mmWave, CRAN, massive MIMO, NFV, hetNets, small cells, and SDN using machine learning.

## I. Introduction
- **Enchanced Mobile Broadband(eMBB)** : 5G aims to provide up to 10Gbps (10x improvement over 4G).
- **Ultra-Reliable Low-Latency Communication (URRLC)** : This for services that require extremely low error rate and low latency. These applications usually do not require a high data rate
- **Massive Machine Type Communications (mMTC)** : IoT requires connectivity standards for high device density with low power. IoT devices operate on battery and are expected to last  10 years.
-  In mobile networks, **80% of the energy is consumed by base stations**. To enhance coverage and capacity, deploying many small cells increases network density, resulting in higher energy consumption.
    -  Network energy consumption fluctuates between peak and off-peak hours. $$\downarrow$$ 
    -  base station contributing to increased energy use when new functions are added. $$\downarrow$$ 
    -  **Network Function Virtualization (NFV)** addresses this by eliminating hardware needs and implementing separate software-based functions. $$\downarrow$$ 
    -  For example In RAN, a single virtual machine for baseband processing and others for core network user policies can share a node $\rightarrow$  more energy-efficient network.
    

## II. BRIEF OVERVIEW OF 5G, ENERGY EFFICIENCY & MACHINE LEARNING
### 5G AND ENABLING TECHNOLOGIES
| Performance | 4G | 5G|
| --- | --- | --- |
| Peak Speed | 1.4 GB/s| 10 GB/s|
| Latency | 40-50 ms | < 10 ms |
| Connectivity |10-10K devices supported/mi^2| 1 million devices supported/mi^2|
| Energy Efficieny |90% more used energy/bit|90% less used energy/bit |
| Mobile data volume| 1/100 Tb/s/Km^2 | 10 Tb/s/Km^2 |

![image](https://hackmd.io/_uploads/r1xlhFPha.png)

**Figure 3. Total energy consumption of 2018 and 2025.**
![image](https://hackmd.io/_uploads/Bki5sFPh6.png)
- **Millimeter waves** ranging from 30GHz to 300GHz $\rightarrow$ offer largerbandwidth for users $\rightarrow$ higher data transmission rates. However, at extremely high frequencies, attenuation increases $\rightarrow$ mmWaves cannot be used for long distance communication
-  **Massive MIMO** is connecting multiple  antennas to a single base station, enhancing spectrum utilization and data rates. 
-  **Heterogeneous Network (HetNet)** deployment includes various radio technologies and legacy systems to offer seamless coverage and capacity.
-  **Ultra Dense Network** is  dense deployment of small cells provide users with better coverage and throughput. While deploying numerous small cells effectively addresses capacity and coverage concerns, it leads to increased costs and management challenges due to the deployment of a large number of base stations.
-  **Software Defined Networking (SDN)** can finely orchestrate and control applications/services across the entire network $\rightarrow$ more efficient network management.
-  **Network Functions Virtualization (NFV)** separates functions (such as firewall or encryption services) from dedicated hardware, transforming them into connectable blocks shifted to virtual switches, servers, or inexpensive hardware. Traditional specialized network hardware is expensive and challenging to program for evolving network needs $\rightarrow$ reducing flexibility. 
-   **Cloud Radio Access Network (CRAN)** offers features such as central processing, energy-efficient infrastructure, real-time computing, and enhanced spectral utilization.
-  **MEC (Mobile Edge Computing)** is similar to CRAN technology, aims to enhance the Radio Access Network (RAN). While CRAN focuses on centralization and cloud services, MEC focuses on decentralization, bringing computation, processing, and storage closer to users. MEC reduces latency and reduce traffic jams in the network.

### MACHINE LEARNING OVERVIEW
![image](https://hackmd.io/_uploads/r1XHiKPh6.png)
- **Supervised learning** is best for addressing channel-related issues, including channel estimation, detection, and understanding its behavior for making future predictions.
- **Unsupervised learning** is best for clustering and spectrum sensing in wireless networks, autonomously solving complex problems without explicit guidance.
- **Reinforcement learning** is best for addressing unknown challenges in networks, especially for tasks like resource allocation and management. It adapts its strategy based on outcomes, systematically learning and enhancing decision-making.


## IV. TAXONOMY
![image](https://hackmd.io/_uploads/BJ_NdkYna.png)
### A. Core Network
**SOFTWARE DEFINED NETWORKING (SDN)**
- The foundation of 5G infrastructure relies on Software Defined Networking (SDN), enabling centralized and intelligent network control through the utilization of software applications. the major advantages of SDN is intelligent networking, resource virtualization, and session management.
- **Few issues in SDN** that needs to be investigated further:
    1.  **an overhead increase because of excessive requests to the controller.** 
    To address congestion, a low-cost load-balanced route management framework (L2RM) is proposed. $\rightarrow$ Adaptive route modification (ARM) triggered by load $\rightarrow$ enhances switch efficiency by updating dynamically and waking up only when necessary, saving cost and energy.
    2. **Overbooking increases the risk of service level agreement (SLA) violations in cloud computing**
    To address this problem, Integrate machine learning with SDN for improved energy efficiency, emphasizing feature extraction to derive relevant data.
    3.  **Switches, ports, and active links consume a lot of power in any SDN.**
    A hybrid energy-efficient routing solution is proposed,employing a supervised and reinforcement learning framework named HyMER. The technique involves feature reduction using supervised learning in the first stage and dynamic routing through Q-learning in the second stage. However, the method relies on extensive training with historical data, potentially introducing bias if training data is insufficient.
    
### B. ACCESS NETWORK
**MASSIVE MIMO**
- As the MIMO concept evolves into 5G, massive MIMO, deploying a larger number of antennas, offers various advantages, including increased throughput, enhanced spectral efficiency, higher signal-to-noise ratio, greater capacity, reduced latency, higher data rates, and improved energy efficiency. However, antennas placement is still an issue in massive MIMO.
- Increasing the bits per Hertz enhances spectrum efficiency, with spatial modulation, particularly massive MIMO, providing higher bandwidth, energy efficiency, and spatial freedom. However, the pilot contamination issue arises from inter-user interference using the same reference signal, especially when cells share frequency blocks. To address this, switching among different pilots, especially within large sequences, helps alleviate the pilot contamination problem in any base station.
- A deep learning approach is utilized for power allocation based on user location, proving the superiority of the max production strategy in complex calculations. Inefficient power allocation methods are addressed using a different neural network with the LSTM layer. While simulations indicate promising results for energy-efficient power allocation, the massive MIMO scenario lacks real-time significance. 

### C. Core Network
**Mobile Edge Computing (MEC)**
- MEC intelligently merges network conditions, location, and radio information to serve users effciently.
-  Integrating MEC with NFV and SDN enhances flexibility and services. The flexible nature of MEC contributes to achieving Ultra-Reliable Low Latency Communication (URLLC) and reaching edge cloud milestones. 
-  Mobile Cloud Computing (MCC) offers end-users advantages through centralized cloud storage resources and computing. However, it encounters challenges like high latency and distance. On the other hand, Mobile Edge Computing (MEC) is distributed, offering lower latency and distance to user equipment but with constraints on storage and computational power.
-  MEC has advantage on computational offloading. It gives benefits in energy consumption, response time, and performance. This is exemplified through three key use cases
    1. **Consumer-oriented services** :  Particularly beneficial for low-latency applications like online gaming and virtual/augmented reality. 
    2. **Operator and third party services** : MEC functions as a gateway for Internet of Things (IoT), streamlining and enhancing the delivery of services.
    3.  **Network performance and QoE improvement services** : improve network performance by delivering real-time information, enhancing Quality of Experience (QoE), and facilitating coordination between the backhaul network and radio components.
-  To address dynamic channel in MEC, Reinforced Learning can be incorporated. This approach is well-suited for handling complex and high-dimensional issues within MEC. Additionally, exploring deep connections within MEC facilitates intelligent decision-making for resource allocation and computational offloading.

## VI. FUTURE DIRECTIONS AND OPEN ISSUES

**1. Combining technologies**
-  Small cells are suitable for dense user populations, while massive MIMO is efficient for less dense environments. Although massive MIMO is usually less energy-efficient than small cells, it becomes more efficient when active antennas use less power than switched-off antennas.
-  Combining Massive MIMO and mmWave achieves a lower power consumption architecture, but further research is needed for dynamic installment and understanding the network's energy efficiency.
  
**2. Harvesting real-time benefits**
- SDN controllers enable real-time monitoring by detaching the central controller from the data plane.
- MEC is a promising option for real-time advantages, managing end-user mobility. 
- Future challenges involve handling multiple nodes and controlling virtual machine migration for guaranteed service delivery.

**3. Softwarization & virtualization**
-  SDN helps NFV connect virtual network functions easily, and NFV helps SDN by virtualizing network functions
- Exploring the integration of MEC with SDN/NFV can address growing user demands and energy constraints.

**4. Machine learning and data relationship**
- Before training, it's essential to align, debug, and clean all data, removing biased values that demand extensive processing.
- Future research should focus on balancing efficient machine learning for wireless networks and simplifying models, particularly in areas where energy efficiency is crucial.

**5. Reinforced learning in real-time environment**
-  It can work even without sample or I/O data, learning from the environment and giving rewards. in complex situations, it faces challenges due to the large storage space, making it difficult to find data in huge databases.
-  Further research is needed to find better ways to store statistical data, especially since traditional input methods can be tricky.

**6. Collaboration & Discovery**
- MEC is a technology located at the user's end, and it needs good communication between different network providers. 
- That show the necessity for a suitable collaboration protocol to access networks despite differing deployment locations.

**7. Front-haul dependency**
- As more people use data, the need for front-haul bandwidth is increasing. But because deploying front-haul is expensive, it creates challenges in expanding infrastructure and increasing costs. This can also reduce energy efficiency. 
- To solve these problems, front-haul needs networks with low delays and large capacity to handle the current capacity issues.

**8. Device-to-Device (D2D) communication**
- energy efficiency is affected by frequent device discovery operations
- That is influenced by protocols that make devices listen and exchange discovery messages frequently.

**9. Need of energy harvesting**
- Densely deployed computational Base Stations in the future will use a lot of energy.
- To address this,  utilizing energy harvesting from renewable sources to power MEC servers $\rightarrow$  extending the network's lifespan.

**10. Performance** 
- Applications heavily dependent on hardware resources or requiring low latency face performance degradation due to their virtualized nature.

**11. RAN and need for intelligence in algorithms**
- Offloading in radio access networks offers advantages such as lower latency, enhanced Quality of Service (QoS) and Quality of Experience (QoE), and automatic network selection. 
- Future improvements should use machine learning to balance energy use and reduce complexity by minimizing repeated information traffic.

## VII. CONCLUSION
- 5G is a diverse network enabled by technologies like virtualization, softwarization, new RANs, and backhaul strategies. These drive extremely low latency, high throughput, and massive connectivity. 
-  Proper implementation of machine learning can optimize 5G network operations while improving energy efficiency. However, there are ongoing challenges that require attention to build highly energy-efficient networks.


















