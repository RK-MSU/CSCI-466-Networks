# RDT (09/20)

## Principles of reliable data transfer

- Packet Loss
  - Buffer Overflow
- Bits become corrupted
  - Interference
  - Cosmic rays
- Reordered
  - Take 2 different paths
  - Retransmitted at the physical layer

## Protocols (Bruce Lee FSM)

[Bruce Lee Ping Pong (Full Version)](https://youtu.be/SncapPrTusA)

**--Image--**>

## Reliable channel

- rdt1.0: reliable transfer over reliable channel
- Assumptions:
  - Unidirectional, long data flows
  - Perfectly reliable channel:
    - No bit errors
    - No packet loss
    - No packet reordering

**--Image--**>

## rdt2.0: Channel with bit errors

- How are errors detected?
  - Checksums: `make_pkt(data, checksum)`, `corrupt(rcvpkt)`
- How do humans recover from communication errors?
  - ACKs, NAKs, and retransmissions: `isACK(rcvpkt)`, `isNAK(rcvpkt)`
- Design sender and receiver FSMs for rdt2.0

> If an error occurs, what would we do? **Repeat**<br><br>Humans have 'positive' acknoledgements in conversation.

**--Image--**>

## Next Part

Send on packet and wait for a response, *this can very slow*. We'd like to send multiple packets and then wait for an acknoledgement.

> Humans speak in full sentences, not one word at a time, and waiting for positive ques.

- What happens if ACK/NAK corrupted?
  - Duplicate delivery, or no retransmission when needed
• How can we deal with corrupted ACKs/NAKs? – Retransmission, but can get duplicate packets
• How to handle duplicate packets?
– Embed sequence numbers in packets:
make_pkt(seq_num, data, checksum), get_seq_num(rcvpkt)
– Only need 0 and 1 for seq_num. Why?
    - Waiting for entire processs to complete - stop and wait protocol
• Come up with sender and receiver FSMs for rdt2.0 with sequence
numbers and retransmissions

-----

- sending duplicates, recievver needs to know this. 
  - sequence numbers in packets

**--Image--**>

> Group talk: Extra step in Reciever...<br><br>Add addition check for packet sequence num - to check for duplicates

##  rdt2.1: sender, handles garbled ACKs

**--Image--**>

## rdt3.0: bit errors and loss

  • New assumption: – packet loss
• How do we know a loss has occurred?
• What can we do about it?
• Approach:
– Sender waits “reasonable” amount of time for ACK
– Retransmits packet if no ACK received in this time
• What if packet/ACK only delayed?
– Duplicate packets ignored at the receiver through sequence numbers
– Receiver specifies sequences number of ACKed packet

### rdt3.0 in action

1 - **--Image--**>

2 - **--Image--**>

## Summary

> Walk aways with: Provide solution of viablity where there is none. Use state transitions diagrams (necessary before you start implementing)
