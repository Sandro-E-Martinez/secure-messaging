# System Components

## 1. Clients (Sender and Receiver)

### Main Functions

#### Sender:

- Generate session keys
- Encrypts messages and metadata
- Send messages and headers to the relay

#### Receiver:

- Request headers from the relay
- Check if the messages are for them using their private key
- Requests complete messages and decrypts them

### Usage of Nostr Keys:

- Public key (npub): Used by the sender to encrypt session keys
- Private key (nsec): Used by the receiver to decrypt session keys

### Technologies Used:

- Frontend: React with Vite
- Encryption: Implemented in Rust, compiled as WebAssembly (Wasm) for efficiency and security

Clients, both sender and receiver, are essential components that interact with relays to send and receive messages securely and privately. They leverage Nostr keys for encryption and decryption, and use modern technologies for a seamless user experience and strong encryption.

## 2. Relay

### Main Functions:

- Stores encrypted messages and headers
- Relays headers to receiving clients
- Send complete messages when the receiver requests it

### Restrictions:

- Does not decrypt messages or metadata
- It does not identify senders or receivers
- Acts only as a neutral intermediary

### Technologies Used:

- Backend: Golang with Gin framework
- Infrastructure: Docker for horizontal scalability

The relay is a core component that facilitates secure communication between clients. It stores and retransmits encrypted messages without accessing their content, ensuring privacy. Its design allows for horizontal scaling to handle high demand.

## 3. Distributed Database

### Main Functions:

- Stores encrypted messages and headers in a distributed manner
- Maintains synchronization between relays
- Ensures persistence and availability of messages

### Restrictions:

- Only store encrypted data
- Does not maintain information about senders/receivers

### Technologies Used:

- Distributed database like CouchDB or similar
- Replication system for synchronization between nodes

The distributed database is a fundamental component that ensures the persistence and availability of encrypted messages across the relay network. Its distributed architecture ensures that data remains accessible and synchronized, while maintaining strict privacy controls by handling only encrypted information.

| [← Sequence Diagram](4-sequence-diagram.md) | [Index](../README.md) | [Chosen Encryption Algorithms →](6-encryption-algorithms.md) |
| :------------------------------------------ | :-------------------: | -----------------------------------------------------------: |
