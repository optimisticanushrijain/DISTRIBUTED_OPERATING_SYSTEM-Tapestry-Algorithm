# DISTRIBUTED_OPERATING_SYSTEM-Tapestry-Algorithm

GOAL: To implement in Elixir using the actor model the Tapestry Algorithm and a simple object access service to prove its usefulness. We have developed a distributed application in this project that built an overlay network using Tapestry APIs with custom implementation for network join and requests routing. Through this, we demonstrated scalable, decentralized object location in peer-to-peer systems.

Technologies used: Elixir, Erlang, Atom

Team Members:
(1) Sahil Bhalla -1699-2193
(2) Anushri Jain – 8764-6425

#To run the code of Tapestry Algorithm, execute the following procedure:

Go to the folder 'project3' using command line tool and type: mix run project3.exs numNodes numRequests. This will start up the application and create a Tapestry network of numNodes. When all peers performed numRequests each, the program can exit. 

where numNodes is the number of peers to be created in the peer to peer system
numRequests is the number of requests each peer has to make. Each peer should send a request/second.

# What is Working:
We were able to generate nodes using GenServers, and then did prefix matching, for the Hexadecimal node ID's. On the basis of how many digits matched, as well as the digit at which matching stopped, we were able to determine the position of a specific PID/Node in the routing table of our current node.

The program successfully prints the routing tables of each node, with its neighboring nodes according to the algorithm, at the correct levels and positions. In addition, the messages are being passed from one node to other node via hops (node connections) and we were able to print the hops (node connections) that must be traversed for delivering the message. But, unfortunately, we were unable to print the maximum number of hops (node connections) that must be traversed for all requests for all nodes

# Largest Network we managed to deal with:
We were able to create a network of 10,000 nodes, with our CPU resource utilization hitting 100%, at a turbo clocked speed of 3.6 GHz. We got the routing tables, for these 10,000 nodes after about 120 seconds.
(Note, we have taken levels from 0, where 0 is the level in which all nodes have a successful prefix match).


