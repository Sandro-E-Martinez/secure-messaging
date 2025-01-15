# Secure Message Flow

## Message Flow Steps

### 1. Message Preparation (Sender)

- Generate unique session key with AES-GCM
- Session key cipher with Nostr public key of the receiver
- Create header with encrypted session key and optional lightweight metadata (e.g. timestamp)
- Encrypts entire message with session key
- Send to relay: header and encrypted message (stored but not sent yet)

### 2. Initial Header Download (Receiver)

- Requests only available message headers from the relay
- Relay sends all headers, lightweight and fast to process

### 3. Header Verification (Receiver)

- Examine each header:
  - Attempts to decrypt session key using its Nostr private key
  - If they successfully decipher it, they know that the message is addressed to them
  - Save message ID for later request

### 4. Full Message Request (Receiver)

- For each message identified as your own in step 3:
  - Sends same header back to relay as reference
  - Relay locates and sends the corresponding full encrypted message

### 5. Decryption of Complete Messages (Receiver)

- Use each decrypted session key to decrypt message content and metadata
- Messages are accessible by receiver in plain text

|     | [← Project Overview](2-project-overview.md) | [Index](../README.md) | [Sequence Diagram →](4-sequence-diagram.md) |
| :-- | :-----------------------------------------: | --------------------: | ------------------------------------------- |
