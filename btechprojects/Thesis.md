---
layout: btechprojects
type: btechprojects
title: Thesis
# All dates must be YYYY-MM-DD format!
date: 2017-05-26
labels:
  - 4G Cellular System
  - Scheduler
---

Here in this project, I will share my thesis project titled ***QoS provisioning Downlink Resource Management in 4G Cellular System***. I will share the objective, motivation, findings, and learnings.

## Summary:
My BTech final year thesis titled .
In this thesis, a Quality of Service aware packet scheduling mechanism called QDRM to manage the downlink spectral resource in an LTE system, has been proposed. This proposed QDRM mechanism allows the eNodeB to search for disposable resource blocks after a preliminary resource allocation to UEs. Then, these disposable resource blocks are reallocated to the traffic flows according to their QCI values and packet latency. In this manner, the delay and bandwidth demands of GBR traffic flows can be satisfied while also preventing non-GBR traffic flows from starvation. 
Through simulations, I have shown that the proposed QDRM mechanism can alleviate packet dropping of VoIP traffic flows, reduce average packet delay of H.264-video traffic flows, and keep relatively higher throughput of non-GBR traffic flows, thus demonstrating its effectiveness.

## Motivation:
Orthogonal Frequency Division Multiple Access (OFDMA) is a preferred technology for downlink mobile broadband access systems as the 3GPP Long Term Evolution (LTE) in downlink, where the diversification of the proposed services (Voice over Internet Protocol, video streaming, gaming or simple web browsing) and higher throughputs are key targets. Therefore, Quality of Service in OFDMA is a key issue for the success of next generation mobile systems. Furthermore, in order to provide different quality of service (QoS) for various types of traffic flows, LTE defines two categories of traffic flows: guaranteed bit rate (GBR) and non-guaranteed bit rate (non-GBR).

Conventional LTE resource management schemes such as MT (Maximum Throughput), PF (Proportional Fair), M-LWDF (Modified Largest Weighted Delay First), and EXP/PF (Exponential Proportional Fair) do not differentiate GBR traffic flows from non-GBR ones, so they may not meet the QoS requirement of GBR traffic flows. The GBR flows have strict delay and bandwidth requirements and therefore need to be prioritized over non-GBR traffic flows.
So, how to efficiently distribute these resource blocks among user equipments (UEs) is a challenging issue, which also significantly affects the system performance of LTE. 

In present thesis project, I have focused on investigating how to efficiently distribute resource blocks among UEs with the following two primary objectives: 
- First, the QoS requirements of GBR traffic flows should be satisfied in order to reduce their packet latency (and also the packet dropping ratio). 
- Second, non-GBR traffic flows can still obtain the necessary amount of downlink resource to prevent them from starvation.
To achieve these two objectives, the project compares different resource allocation mechanisms and finally proposes an Optimized Packet Scheduler (OPS) mechanism for effective resource allocation in LTE systems. Since, as mentioned before, the conventional resource management schemes do not differentiate GBR and Non-GBR traffic, as a result, some of them might end up favouring achievement of high throughput (by favoring GBR traffics), whereas others might emphasize on reducing packet delay. So they may not meet the QoS requirement when both GBR and non-GBR traffic flows are present. Hence the objective is to introduce an Optimized Packet Scheduler mechanism that could take care of all these factors. 
Restating, the idea, is to first give the preliminary allocation of resource blocks to UEs based on their current channel conditions. The eNodeB then calculates a portion of resource to be ‘reallocated’ later (in order to improve the system performance) by referring to the QoS class identifier (QCI) value, the buffer length, and the number of data bits carried by one resource block. Finally, traffic flows compete for such resources according to their head-of-line (HOL) packet delay and QCI values. 

By conducting simulations on Matlab, experimental results demonstrate that our QDRM mechanism can outperform common LTE resource scheduling approaches, in terms of the above two objectives!

## Ideas and References from studying other papers:
- ***A cross layer framework for overhead reduction, traffic scheduling, and burst allocation in IEEE 802.16 OFDMA networks***
WiMAX OFDMA downlink subframes have a 2D channel time structure. The resource allocation from this 2D structure incurs the extra control overheads. It hurt the network performance. The existing method is designing the scheduler in MAC layer and burst allocator in physical layer. Here the overhead reduction is limited. 
(*J. M. Liang, J. J. Chen, Y. C. Wang, and Y. C. Tseng, “A crosslayer framework for overhead reduction, traffic scheduling, and burst allocation in IEEE 802.16 OFDMA networks,” IEEE Transactions on Vehicular Technology, vol. 60, no. 4, pp. 1740–1755, 2011*)

- ***Orthogonal frequency division multiple access in WiMAX and LTE: a comparison***
In this article, we do a detailed comparison of the implementation of OFDMA in LTE and WiMAX. The multiuser diversity advantage of OFDMA is well used in LTE, whereas the frequency diversity advantage is nicely exploited in WiMAX. The physical layer overhead in LTE is significantly better than in WiMAX. The network entry process of an LTE mobile is simpler than in a WiMAX mobile.<br>
(*S. Srikanth, P. A. M. Pandian, and X. Fernando, “Orthogonal frequency division multiple access in WiMAX and LTE: a comparison,” IEEE Communications Magazine, vol. 50, no. 9, pp. 153–161, 2012*)

- ***Efficient eNB deployment strategy for heterogeneous cells in 4G LTE systems***
The recent development of mobile communications, has led to the increment of number of users that network operators need to serve. To cope with the increasing demand of users, the deployment of evolved node base stations (eNB) is an open issue in the present scenario. In our work, focus is on developing a cost-effective and power-efficient eNB deployment framework for Heterogeneous Cellular Networks (HCNs). HCNs are looked upon as an integral part of the mobile communication systems.<br>
(*Y. C. Wang and C. A. Chuang, “Efficient eNB deployment strategy for heterogeneous cells in 4G LTE systems,” Computer Networks, vol. 79, no. 14, pp. 297–312, 2015.*)

- ***Compensation modeling for QoS support on a wireless network***
The compensation model uses different compensation strategies for the different priority classes in conjunction with a multiclass priority fair queuing (MPFQ) algorithm. Simulation results show that the new MPFQ compensation model meets the long-term fairness guarantees and provides an improved flow separation.

- ***Downlink Packet Scheduling in LTE Cellular Networks: Key Design Issues and a Survey***
In this paper an extensive survey on downlink packet allocation strategies recently proposed for LTE networks has been provided, highlighting at the same time key issues that should be considered when designing a new solution. From a spectral efficiency point of view, the best solution is to allocate a RB to the user that is expected to exploit it at the best, thus maximizing the cell capacity. However, every other issues, such as fairness, computational complexity, cell-edge coverage, QoS provisioning, and energy savings, can be solved always at the cost of reducing the overall cell capacity. In this sense, the design of an allocation strategy often lies in the capacity of finding a good trade-off among the system spectral efficiency and the goals that the network operator wants to reach. Having to deal with wireless environment, we need to take into account the variable channel conditions. The dependence of the scheduler working rationales on parameter settings is a problem that need to be carefully addressed. We think that a robust strategies should guarantee the ability to work in very different scenarios. Therefore, it should require no strong parameter settings, or it should at least dynamically adapt such parameters to environmental changes.<br>
(*F. Capozzi, G. Piro, L. A. Grieco, G. Boggia, and P. Camarda, “Downlink packet scheduling in LTE cellular networks: key design issues and a survey,” IEEE Communications Surveys & Tutorials, vol. 15, no. 2, pp. 678–700, 2013*)

## Project Description:

### LTE Architecture:
LTE adopts the concept of traffic flows to provide quality of service (QoS) to different applications, and it classifies all traffic flows into guaranteed bit rate (GBR) traffic flows and non-guaranteed bit rate (non-GBR) traffic flows. As their name suggests, GBR traffic flows (for example, conversational voice and video, or real-time gaming) usually have strict delay and bandwidth demands. Therefore, they have to be prioritized over non-GBR traffic flows so as to meet their demands. Each traffic channels can have diverse QoS demands. This QoS demand of each traffic channel can be related with the packet latency and loss rate. LTE identifies every traffic flow with a scaler identifier called QoS Class Identifier (QCI). 
<br>
LTE divides the downlink spectral resource into multiple resource blocks, where each user equipment (UE) needs to obtain some resource blocks before receiving the data of a traffic flow sent from the eNodeB - how to allocate the resource blocks to UEs plays an important role in LTE downlink performance. And it should be noted that, the LTE standard leaves the implementation of resource-block allocation to manufacturers and researchers.
<br>
<div class="ui medium rounded images">
  <img class="ui image" src="../images/LTEArchitecture.jpg">
</div>
<br>

