# Distributed System: Python, Libraries: Sys, Socket, Picked

**Simple client:** A simple client that connect to a Group Coordinator Daemon (GCD) utilizing TCP/IP connections. The GCD responds with a list of potential group members which my client will send a message to. The responses are printed out and then exits the server.


**Arbitrage Detection with Published quote:** The program implements the Bellman-Ford algorithm listens to currency exchange rates from a price feed and prints out a message whenever there's an arbitrage opportunity available, utilizing UDC/IP connections. As of right now, the arbitrage appears to be detected in the reverse (showing losses instead of profit).


**Distributed Hash Table**: The program implements the Chord system, a P2P lookup service. This system allows any node to join the group when there is no data yet in the DHT and other nodes update their finger tables with each join. The system allows a querier to talk to any node in the network to query a value for a given key or add a key/value pair. Removing a key is not in scope for this lab.


**Bully Algorithms:** The bully algorithm expands on lab 1. The client connects to the GCD and talks to the GCD members to determine who is the leader. The leader is determined by the member with the fewest days till their birthday or, if the birthday is the same, the one with the smalled SU ID (int). The process listens for other members who want to send messages to it. If ELECTION message is received, the higher process sends this message to higher process's, and receives a dictionary of all group members, keyed listen_address with values of corresponding process_ids. An election is started to determine who is the leader. Once the leader is determined, the leader sends a COORDINATOR message stating they are the winner.


	**BitCoin Blockchain:** The program will obtain an old block from the BitCoin blockchain with a P2P connection (TCP/IP). The block numbers corresponds to our SU ID.Tasks:
•	Displays the transactions in block
•	Manipulate one of the transactions in the block to changes its output account. Fix up the block to correctly represent the modified data
•	Show the program-generated report how the hash of the block has changed and way the block would be rejected by peers.
