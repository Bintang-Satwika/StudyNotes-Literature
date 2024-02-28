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

