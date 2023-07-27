This is an Implementation of Gossip Style Membership Protocol - solution to programming assignment for  [Coursera Cloud Computing Concepts, Part 1](https://www.coursera.org/learn/cloud-computing?specialization=cloud-computing)
The application is modelled as a single-threaded simulation engine which can be extended to a real network.

The protocol satisfies:
  - `Completeness`: every non-faulty process must detect every node join, failure, and leave all the time
  - `Accuracy of failure detection`: high accuracy of failure detection for a lossy network

**Functionalities Implemented as part of the Assignment**
  1. Introduction of new peers to the group by use of `JOINREQ` and `JOINREP` messages
  2. Maintaining and updating membership list at each of the peers in the group
  3. Sending Gossip messages to `FANOUT` random members from amongst membership list 
  4. Failure detection by use of `TREMOVE`(time since last heartbeat received) and `TFAIL`(allowing other nodes to remove the failed node)
     1. Single node failure
     2. Multiple node failure
     3. Single node failure under a lossy network. 

#### Instructions to Simulate

```bat
cd .\gossip-membership-protocol
make
./Application testcases/<test_name>.conf
cat dbg.log
```
