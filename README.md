# Secure Messaging System

This project seeks to develop an open source distributed messaging system, with special emphasis on privacy. The system is based on a distributed network of relays that facilitate the secure transmission of messages using the Nostr protocol for identity management.

When it comes to private messaging between two individuals, several options are available, each with its own set of advantages and disadvantages. There is no universally perfect service or application for fully private messaging. The existing options are predominantly centralized (with the exception of Mastodon), do not provide end-to-end encryption (except for WhatsApp and Signal messages), and metadata is generally accessible to the service provider.

We require a service that simultaneously meets the criteria of permissionlessness,
decentralization, platform agnosticism, and the encryption of both data and metadata.

Through the utilization of NOSTR and novel concepts we have developed, we believe we have identified a potential solution to this challenge.

To address the decentralized and permissionless concerns, we will employ relays similar to those employed by NOSTR.

To resolve the encryption challenge, we will employ a combination of encryption methods utilizing NOSTR NPUB/NSEC.

To address the metadata encryption issue, we will conceal the identity of the sender and recipient by embedding the messages among other encryp

# Documentation

## Index

1. [Introduction](docs/1-introduction.md)
2. [Project Overview](docs/2-project-overview.md)
3. [Secure Message Flow](docs/3-secure-message-flow.md)
4. [Sequence Diagram](docs/4-sequence-diagram.md)
5. [System Components](docs/5-system-components.md)
6. [Encryption Algorithms](docs/6-encryption-algorithms.md)
7. [Technical Aspects](docs/7-technical-aspects.md)
8. [Use Cases](docs/8-use-cases.md)
9. [Product Requirements Document](docs/9-prd.md)
10. [Development Roadmap](docs/10-development-roadmap.md)
11. [Budget](docs/11-budget.md)
12. [Distribution of Additional Responsabilitites](docs/12-distribution-of-additional-responsabilitites.md)
