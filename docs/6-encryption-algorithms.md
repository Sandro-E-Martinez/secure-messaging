# Chosen Encryption Algorithms

In this system, encryption algorithms have been carefully chosen that work together to provide
the highest level of security and privacy. A hybrid encryption approach has been chosen,
combining the strengths of symmetric and asymmetric methods, in order to ensure the
confidentiality of messages and efficiency in the encryption and decryption process.

The selected algorithms and their function within the system are as follows:

## 1. Symmetric Encryption: AES-GCM

### Main Features

- AES (Advanced Encryption Standard): Widely used and highly secure encryption standard
- GCM Mode (Galois/Counter Mode):
  - Provides confidentiality, protecting message content
  - Provides authenticity and integrity through authentication tag

### Reasons for Choice

- Speed: Extremely fast and efficient on all devices
- Security: Resists common attacks and meets modern standards
- Authenticity: GCM ensures message integrity

### Role in System

- Encrypts message content and metadata using unique session keys
- Ensures message security even if intercepted during transmission

AES-GCM is an essential component of a secure messaging system. Its combination of speed, security, and authenticity make it the ideal choice for encrypting message content. By generating a unique session key for each message, AES-GCM ensures that even if a message is intercepted, its content will remain confidential. Furthermore, GCM mode adds an additional layer of protection by providing an authentication tag that verifies the integrity of the message,ensuring that it has not been altered in transit. With AES-GCM, users can be confident that their messages are secure and protected from end to end.

## 2. Asymmetric Encryption: ECC (Elliptic Curve Cryptography)

### Main Features

- Uses elliptic curves to perform cryptographic operations
- It offers the same security as other asymmetric algorithms (such as RSA) but with smaller keys, ideal for devices with limited resources.

### Reasons to choose ECC:

- Efficiency: Faster and less resource intensive than RSA, especially in key generation and verification
- Compact size: Smaller keys and signatures, reduces the size of encrypted messages
- Broad Support: Compatible with modern standards and widely adopted

### Role in System

- The sender encrypts the AES-GCM session key with the receiver's public key (Nostr npub)
- Only the receiver, with his private key (Nostr nsec), can decrypt this session key

ECC plays a crucial role in the system by enabling asymmetric encryption of AES-GCM session keys. By using the Nostr public keys (npub) of receivers, senders can securely encrypt session keys, ensuring that only the intended receiver, who possesses the corresponding private key (nsec), can decrypt them. This approach leverages the efficiency and compact size of ECC, making it particularly suitable for resource-constrained environments such as mobile devices.

Furthermore, ECC’s broad support and compatibility with modern standards ensure its long-term viability in the secure messaging system. By using ECC, the system can establish a secure channel for session key exchange, further enforcing the privacy and confidentiality of end-to-end communications.

## 3. Hybrid Encryption: AES-GCM + ECC

### Why use a hybrid approach:

- Speed and efficiency:
  - AES-GCM is fast and efficient for encrypting large amounts of data, such as entire messages
- Security in key distribution:
  - ECC ensures that the session key (used in AES-GCM) can only be decrypted by the receiver
- Scalability:
  - It allows to manage secure communications between multiple users without pre-shared keys

### Hybrid encryption flow:

1. The sender generates a unique session key (AES-GCM)
2. The message and metadata are encrypted using AES-GCM with this session key
3. The session key is encrypted with the receiver's ECC public key (provided by Nostr)
4. The encrypted packet is sent to the relay, where it remains inaccessible until the
   receiver decrypts it

The hybrid encryption approach combines AES-GCM and ECC to create a secure and efficient messaging system. AES-GCM quickly encrypts messages, while ECC securely encrypts AES-GCM session keys. This eliminates the need to share symmetric keys beforehand and improves scalability. The system ensures message confidentiality at all times, as only the receiver can decrypt session keys with their ECC private key. Hybrid encryption offers an optimal balance between speed, security, and scalability.

### Advantages of Hybrid Encryption System:

1. End-to-end security: Only the receiver decrypts messages, even if they are intercepted.
   Hybrid Encryption System:
2. Complete privacy: The relay cannot read or infer information from messages or headers.
3. Client-side efficiency: AES-GCM enables fast encryption, even on mobile devices.
4. Simplified key management: Nostr eliminates the need for an additional system for
   public/private keys.
5. Wide Compatibility and Scalability: Adopted standard algorithms ensure seamless
   interoperability and growth.

| [← System Components](5-system-components.md) | [Index](../README.md) | [Additional Technical Aspects →](7-additional-aspects.md) |
| :-------------------------------------------- | :-------------------: | --------------------------------------------------------: |
