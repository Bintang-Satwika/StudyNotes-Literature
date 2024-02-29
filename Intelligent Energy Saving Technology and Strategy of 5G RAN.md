# Intelligent Energy Saving Technology and Strategy of 5G RAN

## ABOUT

| item | information |
| --- | --- |
| Paper Link |https://ieeexplore.ieee.org/document/9828681 |
| Authors |Zhirong Zhang, Mingshuo Wei, etc.|
| Date of Publication | 25 July 2022|
|type | Conference :  Bilbao, Spain|
| total pages | 6 pages |
| keywords | 5G RAN; Energy Saving; AI; MIMO; KPI |

The paper outlines the requirements and scenarios for 5G RAN energy conservation, analyzes the underlying principles and core technologies. Additionally, it explores the integration of AI technology and proposes an evaluation system for assessing energy-saving measures in 5G RAN.

## I. REQUIREMENTS AND SCENARIOS OF 5G RAN ENERGY SAVING
The development of 5G technology has led to an increase in mobile data traffic, requiring the adoption of key technologies such as high frequency and large-scale antenna in 5G RAN. However, 5G RAN's energy consumption is 3 to 5 times that of 4G RAN.

## II. KEY FACTORS OF 5G RAN ENERGY CONSUMPTION
Over 60% of the energy consumption in 5G RAN is from main equipment, and the AAU (Active Antenna Unit) accounts for over 80%. Consequently, energy-saving technologies primarily target optimizing the energy efficiency of AAU.

 ### A. AAU Energy Consumption Analysis
 <img width="302" alt="image" src="https://github.com/Bintang-Satwika/Paper_Literature/assets/87467666/565ff91d-d9f7-4e70-b100-83273c232c1c">

To reduce AAU energy consumption, improving the energy efficiency of the power amplifier module, digital baseband, and transceiver. This involves improving chip performance and integration, adopting advanced technologies like 7nm and 3nm, enhancing integration and processing capabilities, and reducing chip area and quantity.

### B. BBU (Baseband Unit) Energy Consumption Analysis

- The BBU (Baseband Unit) comprises the physical layer, the second $\rightarrow$  MAC (Media Access Control), RLC (Radio Link Control), and PDCP (Packet Data Convergence Protocol), and third layer $\rightarrow$  RRC (Radio Resource Control).
- In the uplink, the BBU receives air interface data from AAU, demodulates and decodes it, and subsequently sends the service and control data to the 5GC (5G Core Network) through the  Next Generation (NG) interface. 
-  in the downlink, the BBU receives service and control data from 5GC through the NG interface, encodes and modulates baseband data, and then transmits antenna data to AAU using eCPRI (enhanced Common Public Radio Interface).
- The 5G BBU includes a main control unit, baseband processing unit, and fan unit. The main power consumption in the BBU system comes from the baseband processing unit.
- <img width="356" alt="image" src="https://github.com/Bintang-Satwika/Paper_Literature/assets/87467666/38078db8-cb9c-4a2d-81ce-73d83ab1c2bd">

- To achieve BBU energy efficiency:
    1. enhance the processing of individual baseband boards by improving chip performance and integration. Utilize advanced technologies, such as 7nm and 3nm, to boost integration and processing, thereby reducing chip area and quantity to decrease energy consumption. 
    2. On existing BBU platforms, dynamically reduce the service processing capability of the baseband processing unit during idle conditions in alignment with user loads. This allows for a dynamic reduction in BBU power consumption.

## III. ENERGY SAVING PRINCIPLE OF 5G RAN

### A. Dynamic Scaling Principle
- **Service-based resource scaling** : The system achieves real-time dynamic scaling by allocating resources in time, frequency, spatial, and power domains, guided by scenario-based network KPI (Key Performance Indicator) and QoS (Quality of Service) requirements.
- **Power consumption scaling with resources** : Reducing resource consumption, such as bandwidth, channels, and transmit power, should lead to a proportional decrease in RAN power consumption.
### B. Trade-off Principle
- The energy-saving process often involves adjusting network resources, which directly influence network performance. Reducing resources enhances energy savings, but affects network performance.
- In leisure scenarios, such as at night, a performance margin exists. Prerequisites involve analyzing the impact of energy-saving technologies through AI modeling. AI model ensures basic network coverage, and establishing a mapping relationship between energy-saving and experience KPIs to find the optimal balance.
- To reduce terminal power consumption, 5G RAN adapts public signaling interaction, often increasing 5G RAN computational cost. Strict IoT terminal requirements for low power consumption worsen this situation. While terminals can save energy by selectively listening to network messages, the network can't easily reduce the frequency of these messages.
### C. Scenario based Demand Principle
The diverse design constraints and user experiences in various scenarios pose unique challenges for energy-saving in 5G RAN. To address this, it is essential to establish scenario-specific energy-saving goals, analyze key technologies, and ensure performance guarantees. 

## IV. ENERGY SAVING TECHNOLOGY FOR 5G RAN
### A. Traditional engergy-saving technology of 5G RAN
1. **Hardware energy-saving technology of 5G RAN**
Hardware energy saving in 5G RAN targets reducing base power consumption and enhancing energy utilization of 5G RAN.The energy-saving scheme of base station hardware mainly considers the following aspects:
    - utilizing new semiconductor processes (5 or 7 nm)
    - Improve the integration of AAU hardware system
    - new materials and processes related to the  energy saving of 5G RAN, such as Gallium Nitride (GaN) to optimize AAU power amplifier efficiency.

2. **Software energy-saving technology of 5G RAN**
Software energy-saving in 5G RAN optimally allocates system resources through software configuration adjustments, aiming to achieve energy-saving and consumption reduction.
The main software energy saving technology of 5G RAN:
    1. **Symbol shutdown**:
    real-time deactivation of power-consuming components like PA and RF modules when there is no data on downlink symbols, so minimize the power consumption.
    2. **Channel shutdown**:
    5G RAN automatically shuts down transmit channels when cell load is below a threshold, adjusting common channel power to minimize impact on coverage and service.
    3. **Carrier shutdown**:
    During low-demand periods like at night, some carriers can be shut down to reduce energy consumption. When the service load is low, users shift from capacity to basic cells, enabling capacity cells to be shut down. If the service load increases, capacity cells can be restarted to restore the network's capacity.
    4. **Deep Sleep**:
    When the AAU is in deep sleep state, only the eCPRI(enhanced Common Public Radio Interface) which communicates with BBU is kept-alive, and other hardware modulesare shut down.

### B. AI-Based energy-saving technology of 5G RAN
1. **Energy Saving Scenario Identification**:
   The model employs AI's correlation and clustering model, utilizing historical data like wireless resource usage, weather conditions, traffic users, and service loads to establish energy-saving scenarios. 
3. **Energy Saving Scenario Identification**:
     The service traffic model utilizes neural networks to establish mapping relationships between historical KPIs, related cell information, and environmental factors, providing insights into the characteristics of the service model.
5.  **Test data of AI-Based energy-saving technology of 5G RAN**:
      In August 2021, China Telecom conducted a test on AI-based energy-saving technology for 5G RAN in Chengdu. The results revealed a 31.08% energy-saving benefit when employing AI energy-saving based on load forecasting.
6. **AI-Based cooperative energy-saving technology of RANs**:
     RAN's energy-saving method involves using historical data from nearby base stations in an AI model for joint prediction, improving traffic accuracy. However, the AI energy-saving model is experimental, and collaborative RAN energy-saving requires development after the basic model matures. If cooperative RANs are from different manufacturers, the AI model needs extensive learning.

## V. ENERGY EFFICIENCY EVALUATION SYSTEM FOR 5G RAN
- The power consumption evaluation module calculates power usage using existing network counters. It is based on power consumption and traffic models, collecting KPI and average PRB usage data through OMC measurement tasks for actual 5G RAN traffic and power consumption.
- The energy efficiency evaluation system aims to assess the effectiveness of energy-saving technologies and strategies in 5G RAN without affecting network performance.

### Conclusion
- The paper discusses about 5G RAN energy saving, analyzing key factors, principles, and core technologies.
- AI technology offers the potential to optimize resource scheduling, enhance user experience, reduce operational costs, and boost market competitiveness.
