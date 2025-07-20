RIP is a distance-vector routing protocol used by routers to share information about networks they can reach. It’s based on the number of hops (routers) a packet must pass through to reach a destination.

Hop Count = Metric (lower = better)

Maximum Hop Count = 15 (16 = unreachable)
--------------Configuration------------------

In router0,

#enable
#configure terminal
router rip
version 2
network 192.168.1.0
network 192.168.2.0   -----> Advertising the directly connected networks

*Router0 will advertise it only to RIP enabled routers

-Likewise configure router1,router2 with their respective directly connected networks for RIP protocol

-Test it pinging PC2 from PC0 and vice versa.


--------------------------Limitations of RIP-----------------------

1.Hop Limit - max 15 hops
2.Slow Convergence
3.Sends routing updates every 30 seconds (entire table)
4.Poor Scalability

--------------------------Where to use RIP protocol----------------------------

1.Very small networks with few routers.
2.Lab environments
3.Not recommended for Real world production environment 