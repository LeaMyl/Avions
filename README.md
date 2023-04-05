# Hub Location Network Optimization

## Introduction
The hub location problem (HLP) is one of the novel and thriving research areas in location theory. 
In order to satisfy a demand, the HLP involves the movement of people, commodities, or information between required origin–destination pairs. 
Hubs are applied to decrease the number of transportation links between origin and destination nodes. 
For example, a fully connected network with *k* nodes and with no hub node has *k*(*k*-1) origin-destination links.

However, if a hub node is selected to connect all other nodes (non-hub nodes, also known as spokes) with each other, 
there will only be 2(*k*-1) connections to serve all origin-destination pairs. 
This idea can be extended to a network with more than one hub node, called a multiple-hub network. 
Thus, by using fewer resources, demand pairs can be served more efficiently with a hub network than with a fully connected structure.

The costs of a hub network depend on its structure. The total distance of arcs connecting the whole network might be less in a hub network, 
but the total travel distance may be greater since there is no guarantee that the number of people, merchandise, 
or information moving on the hub-to-hub connections are greater than those moving between hubs and spokes. 
Therefore, it is very complicated to determine the location of hub facilities as well as the allocation scheme of clients to them.

It seems that the telecommunication industry is originally one of the oldest users of the hub network concept. 
However, logistic systems, airline industry and postal companies are one of the main users of hub location network optimization.  
Today, there are many other areas that can take advantage of hub concept like maritime industry, 
freight transportation companies, public transit, and message delivery networks.

![Hub location network.](Figure1.pdf "Hub location network")
*Figure 1: Hub location network*

![A sample of a hub network in air transportation.](Figure2.pdf "A sample of a hub network in air transportation.")
*Figure 2: A sample of a hub network in air transportation.*


## Hub network properties
Each hub network is caracterized by particular structural properties. 
In the following, some of the main features are provided.

- **Single Allocation vs. Multiple Allocation**. 
In single allocation, each spoke must be allocated to exactly a single hub, while in multiple allocation, 
each spoke can be allocated to more than one hub. Figure 3 shows the difference between these two features.

![Single allocation vs. multiple allocation](Figure3.pdf "Single allocation vs. multiple allocation")
*Figure 3: Single allocation vs. multiple allocation*

- **Complete vs. Incomplete Hub Network**. In a complete hub network, the graph of hubs is complete and all the hubs are directly connected. In an incomplete hub network, the graph of hubs is incomplete but there is at least one indirect path between each pair of hubs. Figures \ref{Figure 4}a to \ref{Figure 4}c illustrates three different types of incomplete hub networks: a tree, a ring and a general hub network. A tree structure is a graph where no cycle can be found. An incomplete hub network that does not have a ring or tree structure is called general network. Figure \ref{Figure 4}d depicts a complete hub network.

![Various hub graphs](Figure4.pdf "Figure 4")

- **Capacitated vs. Uncapacitated Hub Network**. In a capacitated hub network, a limited number/volume of flows can enter the hub while in the uncapacitated network, the hubs can process infinite number/volume of flows.

## Problem statement

Consider a transportation/telecommunication network that contains a set of origin/destination nodes and the need of transferring a flow between each pair of origin-destination (O-D) nodes. Each node can be an origin or a destination at the same time. The aim is to **locate** a set of nodes as hubs and to **allocate** the remaining nodes (spokes) to the located hub to minimize the network's total cost (i.e., fixed and variable costs).

### Assumptions

You are provided with the following information/assumptions:

- The location of the nodes is fixed,
- Each spoke should be allocated to only one hub (single allocation)
- All the spokes should be allocated to a hub
- There is a fixed cost for locating a hub
- There is a variable cost, per the quantity flows, transferred through the network
- Transferring flow between hubs takes advantage of a discount factor (transferring the flow in big volumes and lower costs)
- Each hub has finite capacity.