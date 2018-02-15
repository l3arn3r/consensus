# consensus

This is a a distributed consensus algorithm given a graph of “trust” relationships between nodes. This is an alternative method of resisting sybil attacks and achieving consensus; it has the benefit of not “wasting” electricity like proof-of-work does.

Nodes in the network are either compliant or malicious. CompliantNode class(which implements a provided Node interface) that defines the behavior of each of the compliant nodes. The network is a directed random graph, where each edge represents a trust relationship. For example, if there is an A → B edge, it means that Node B listens to transactions broadcast by node A. We say that B is A’s follower and A is B’s followee.

Each node should succeed in achieving consensus with a network in which its peers are other nodes
running the same code.

Each node will be given its list of followees via a boolean array whose indices correspond to nodes in
the graph. A ‘true’ at index i indicates that node i is a followee, ‘false’ otherwise. That node will also
be given a list of transactions (its proposal list) that it can broadcast to its followers. Assume that all transactions are valid and that invalid transactions cannot be created.
