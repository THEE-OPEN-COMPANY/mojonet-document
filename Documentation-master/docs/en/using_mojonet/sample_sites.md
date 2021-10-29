# Sample mojonet sites

## mojoHello

The homepage of mojonet

- Lists all added sites: Title, Peer number, Modification date, etc.
- Site actions: Update, Pause, Resume, Delete, Check Files and Save as .zip
- Clone sites to have your own blog / forum
- mojonet Statistics
- If an update is available, mojonet can be updated with one click



---

## mojoBlog

Self publishing blog demo

- Inline content editor
- Markdown syntax
- Code syntax highlighting
- Site signing & publishing through the web interface

How does it work?

- `data.json` contained within site files contain blog posts and comments. Each user has their own.
- Upon pressing `Sign & Publish new content`, the blogger is asked for the site private key (displayed when [creating a new site using mojonet.py siteCreate command](create_new_site/))
- Your mojonet client signs the new/modified files and publishes directly to other peers
- The site will then be accessible until to other peers to view


---

## mojoTalk

Decentralized, P2P forum demo

- Post and comment creation, modification, deletion and upvoting
- Commenting and content modifications pushed directly to other peers
- Only you can sign and modify your own files
- Real time display of new comments

How does it work?

- To post and comment you have to request a certificate of registration (a cryptographic sign) from a mojoID provider
- After you have the certificate you can publish your content (messages, posts, upvotes) directly to other peers


## mojoMail

End-to-end encrypted, distributed, P2P messaging site. To improve privacy it uses a BitMessage-like solution and will not expose the message recipient.

- Using ECIES for secret exchange, AES256 for message encoding
- When you first visit the site, it adds your public key to your data file. At that point anyone is able to send a message to you
- Everyone tries to decrypt every message, this improves privacy by making it impossible to find the message recipient
- To reduce per message overhead and increase decryption speed, we re-use the AES key, but a new IV is generated every time



---

## mojoMe

Decentralized, Twitter-like P2P social network.

- Stores user information in mojoMe user registry
- Stores posts and comments in MergerSites called Hubs
- Upload images as optional files
- Real time display of feed activity





## mojoChat

The finished site for the tutorial of creating a server-less, SQL backed, real-time updated P2P chat application using mojonet in less than 100 lines of code.

- Uses mojoID certificate for authentication
- Stores messages in a SQLite database
- Posts messages and distribute directly to other users in real-time
- Real-time update the messages as they arrive

