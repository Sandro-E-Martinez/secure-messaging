# Use Cases

## Use Case 1: End-to-End Private Messaging

1. Example:

   - A user (Sender) needs to send a securely encrypted message to another user (Receiver), ensuring that only the receiver can read it.

2. Flow:

   - The sender encrypts the message using the receiver's public key and sends it to the relay.
   - The receiver periodically queries the headers available in the relay and verifies using its private key which ones are intended for it.
   - The receiver downloads the encrypted message and decrypts it locally using his private key.

3. Result:

   - The message is read only by the intended receiver, ensuring end-to-end confidentiality.
   - Neither the relay nor third parties can access the content of the message.

Practical examples:

1. A Lightning node operator needs to communicate privately with other operators to coordinate the opening of new channels and discuss routing strategies, without leaving any traces of its infrastructure or capabilities on public communication channels.

2. A crypto protocol developer is working on privacy improvements and needs to share sensitive findings with other contributors before making his work public, preventing his ideas from being exposed prematurely or competitors from getting ahead of them.

3. A Bitcoin investor needs to discuss multi-signature custody strategies with trusted partners, sharing details about wallet configurations and security procedures without exposing this information to media that could be monitored.

## Use Case 2: Messaging with Integrated Lightning Payments

1. Example:

   - A user wants to send a payment to another user along with a message.

2. Flow:

   - The sender sends an encrypted invoice request to the receiver
   - The receiver generates and sends back an encrypted Lightning invoice
   - The sender makes the payment using the invoice received
   - The message is encrypted and attached to the payment confirmation.
   - The relay processes the Lightning transaction and verifies the payment
   - Once payment is confirmed, the encrypted message is released to the receiver
   - The receiver decrypts the message and confirms receipt of payment

3. Result:

   - Message delivered privately to the receiver
   - Payment successfully processed via Lightning Network
   - Transaction completed with confirmation for both parties

Practical examples:

1. A Bitcoin technical analyst shares private trading signals for which he charges in satoshis. His subscribers receive personalized analysis confidentially and pay instantly for each signal, keeping both the analysis and the transaction private.

2. A privacy service provider (such as node setup, VPN, or private server) offers technical consultations. Customers pay in satoshis and receive detailed setup instructions privately, protecting both the provider's know-how and the customer's identity.

3. A security researcher discovers vulnerabilities in crypto protocols and charges to privately share the details with development teams before public disclosure. Payments and communication are kept confidential to protect sensitive information until the issue is fixed.

## Use Case 3: Confidential Business Messaging with Payment

1. Example:

   - A company needs to share sensitive messages with a client/supplier
   - The message must be accessible only by prepayment on the Lightning Network

2. Flow:

   - The sender encrypts the message and sets the price in satoshis
   - The receiver generates a Lightning invoice for payment
   - Upon confirming payment, the relay releases the decryption key
   - The receiver downloads and decrypts the message locally

3. Result:

   - Message delivered securely and privately
   - Payment confirmed and recorded on Lightning Network
   - Transaction completed without revealing identities

Practical examples:

1. A crypto law firm provides legal advice on Bitcoin regulations in different jurisdictions. Clients pay in satoshis to receive specific private consultations, keeping their regulatory compliance strategies and expansion plans confidential.

2. An operational security (OPSEC) expert offers customized audits for companies that handle Bitcoin. Companies pay to receive confidential assessments of their key handling and custody protocols, ensuring that identified vulnerabilities remain private.

3. A research firm specializing in on-chain analysis sells custom reports on Bitcoin flows and Lightning Network patterns. Institutional clients pay for specific insights they need to keep private for competitive advantage.

## Use Case 4: Private Communication on Channels (Broadcast)

1. Example:

   - A sender wants to send a message to a channel (for example, a company or group) so that only members with access to the channel and the appropriate nsec can decrypt and read the contents.

2. Flow:

   - The sender encrypts the message using the channel's public key.
   - The sender publishes the encrypted message to the Relay.
   - Channel members request the Relay.
   - Channel members download all messages available in the Relay.
   - Members attempt to decrypt all downloaded messages using the channel's private key.
   - Messages that were encrypted with the channel's public key can be successfully decrypted and read by users.
   - Messages that cannot be decrypted remain inaccessible and are automatically discarded.

3. Result:

   - Efficiently broadcast messages without the need for subscriber lists (passive subscription).
   - Only members with the channel's private key (nsec) can decrypt and read messages.
   - The anonymity of the senders and receivers is maintained in the Relay.

Practical examples:

1. A company uses a private channel to share important announcements with its employees in different offices. Updates, such as changes in internal policies or corporate news or sensitive and/or confidential information, are encrypted and can only be decrypted by employees with access to the private key, ensuring the confidentiality of the information.

2. A school uses a private channel to distribute class materials, such as lessons and exercises. Only students enrolled in the course, with access to the private key, can decrypt and download the content, granting exclusive access.

3. A premium news outlet offers exclusive content to paying subscribers. Articles and analysis are shared on an encrypted channel, and only subscribers with the private key can decrypt and read the posts, protecting the value of their subscription model.

| [← Additional Aspects](7-additional-aspects.md) | [Index](../README.md) | [PRD →](9-prd.md) |
| :---------------------------------------------- | :-------------------: | ----------------: |
