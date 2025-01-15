# Development Roadmap

### Phase 1: MVP Web

- Core functionality in web app
- Basic encryption system
- Minimal web UI

#### User Stories Web:

- US1: Nostr key integration (21h)

```
As a user
I want to be able to use my existing Nostr keys (npub/nsec)
To be able to send and receive secure messages
```

- US2: Nostr key validation (10h)

```
As a user
I want to be able to verify that my Nostr keys are valid
To ensure that I will be able to send and receive messages correctly
```

- US3: Sending an encrypted basic message from the web (31h)

```
As an authenticated user
I want to be able to send encrypted messages to other users
To keep my communications private
```

- US4: Reception of basic encrypted message on the web (31h)

```
As a recipient user
I want to be able to receive and view encrypted messages
To read communications addressed to me
```

- US5: List of web messages (21h)

```
As a user
I want to see a list of my encrypted messages
To manage my communications
```

- US6: Identity verification through Nostr (16h)

```
As a user
I want to be able to verify the authenticity of other users' Nostr (npub) keys
To ensure that I am communicating with the rightful owner of said key
```

- US7: Message encryption with AES-GCM (26h)

```
As a system
I want to encrypt messages using AES-GCM
To ensure confidentiality of content
```

- US8: Session Key Encryption with ECC (26h)

```
As a system
I want to encrypt session keys using ECC
To ensure secure key distribution
```

- US9: Decryption of received messages (31h)

```
As a receiving user
I want to be able to automatically decrypt received messages
To read the content transparently
```

- US10: Web Notifications of New Messages (21h)

```
As a user of the web application
I want to receive notifications in the browser of new messages
To be informed of
```

- US11: Basic messaging web interface (52h)

```
As a user
I want a simple and intuitive web interface
To manage my communications efficiently
```

- US12: Web performance optimization (31h)

```
As a web user
I want the web application to run smoothly and efficiently
To have a good experience even with slow connections or limited devices
```

- US13: Web Responsive Interface (42h)

```
As a web user
I want an interface that adapts to different screen sizes
To use the application comfortably from any device with a browser
```

### Phase 2: MVP Mobile

- Hybrid app development (React Native)
- Adaptation of core functionalities for mobile
- Mobile-optimized UI/UX

#### User Stories Mobile:

- US14: Basic mobile interface (62h)

```
As a mobile user
I want a mobile-friendly interface
To access the system from my phone
```

- US15: Sending/receiving messages on mobile (42h)

```
As a mobile user
I want to be able to send and receive encrypted messages from my phone
To keep my communications secure on the move
```

- US16: Mobile push notifications (31h)

```
As a mobile user
I want to receive push notifications of new messages
To be informed of incoming communications
```

- US17: QR code scanning (21h)

```
As a mobile user
I want to be able to scan QR codes of contacts
To add contacts easily
```

- US18: Local storage management (31h)

```
As a mobile user
I want to be able to manage local message storage
To optimize space on my device
```

- US19: Cross-platform synchronization (52h)

```
As a user
I want to sync my messages between web and mobile devices
To maintain a consistent experience across all platforms
```

- US20: Mobile Performance Optimization (42h)

```
As a mobile user
I want the app to run smoothly and efficiently
To have a good experience even on devices with limited resources
```

- US21: Adapted touch interface (31h)

```
As a mobile user
I want an interface optimized for touch interaction
To use the app comfortably on small screens
```

- US22: Mobile permit management (31h)

```
As a mobile user
I want to control app permissions on my device
To protect my privacy and system resources
```

- US23: Mobile backup of keys and messages (31h)

```
As a mobile user
I want to be able to back up my passwords and messages securely
So I don't lose important information when changing devices
```

### Phase 3: Advanced Features

- Implementation of private channels with specific encryption for groups
- Development of a system of extensions and documented APIs
- Framework for community contributions
- Privacy-preserving metrics system

#### Advanced User Stories:

- US24: Private multi-platform channels (78h)

```
As a user
channels
I want to be able to create and participate in cross-platform encrypted private
To securely share content with specific groups on both web and mobile
```

- US25: Plugins and extensions system (120h)

```
As a developer
I want to be able to create and publish extensions for the system
To add new functionality while maintaining the basic privacy and security
```

- US26: Documented public APIs (68h)

```
As an external developer
I want access to well-documented APIs
To integrate new services and functionalities with the system
```

- US27: Anonymous usage metrics (57h)

```
As a system administrator
I want to obtain anonymized usage metrics
To improve the service without compromising user privacy
```

- US28: Improvement proposal system (47h)

```
As a member of the community
I want to be able to propose and discuss improvements to the system (similar to NIPs)
To contribute to the collaborative development of the project
```

### Phase 4: Privacy and Scalability

- Implementation of advanced anonymization techniques
- Temporary key system for greater privacy
- Optimization of the distributed relay network
- Implementation of camouflage through data volume
- Development of an economic model for operators
- Comprehensive security audits

#### User Stories:

- US29: Shipping Delegation (52h)

```
As a user
I want to be able to delegate the sending of messages to third parties
To increase my anonymity on the network
```

- US30: Disposable key system (42h)

```
As a user
I want to be able to generate temporary keys
For specific communications that require greater privacy
```

- US31: Optimization of distributed relays (78h)

```
As a relay operator
I want to implement an optimized distributed relay system
To ensure horizontal scalability and high availability of the service
```

- US32: Privacy implementation by data volume (62h)

```
As a system administrator
I want to implement the "privacy through data volume" strategy
To camouflage real messages among the encrypted traffic existing in the Nostr network
```

- US33: Incentive system for relay operators (52h)

```
As a relay operator
I want to be able to monetize specific services via BTC second layers
To maintain a sustainable ecosystem of nodes on the distributed network
```

- US34: Security audits and penetration testing (104h)

```
As a system administrator
I want to perform regular security audits and penetration tests
To identify and fix potential vulnerabilities in the system
```

## Estimates Summary (PM, Dev, QA)

### Total per Development Phase:

- Phase 1 (MVP Web): 359 hours
- Phase 2 (MVP Mobile): 374 hours
- Phase 3 (Advanced Features): 369 hours
- Phase 4 (Privacy and Scalability): 390 hours

**Total 1,492 development hours**

### Total per Project Management Phase:

- Phase 1 (MVP Web): 90 hours
- Phase 2 (MVP Mobile): 94 hours
- Phase 3 (Advanced Features): 92 hours
- Phase 4 (Privacy and Scalability): 98 hours

**Total 374 project management hours**

### Total per QA Phase:

- Phase 1 (MVP Web): 72 hours
- Phase 2 (MVP Mobile): 75 hours
- Phase 3 (Advanced Features): 74 hours
- Phase 4 (Privacy and Scalability): 78 hours

**Total 299 quality assurance hours**

## Resources needed:

- 1 Frontend developer
- 2 Backend developers
- 1 Cryptography engineer
- 1 DevOps engineer
- 1 Project Manager
- 2 QA Testers

## Time

The initial estimated duration of the project is 9 to 10 months. This estimate may vary depending on the prioritization of the backlog and the number of sprints to be worked on during the project.

| [← PRD](9-prd.md) | [Index](../README.md) | [Budget →](11-budget.md) |
| :---------------: | :-------------------: | -----------------------: |
