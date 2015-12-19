# Distributed Linkback Graph specification 0.1

This is a proposal for a system for publishing open data in an open, linked, collaborative and distributed manner.
It is a way for building a decentralized graph data store, that has pseudo-two-way links.
It is based on the Hypertext Transfer Protocol (HTTP) and Javascript Object Notation (JSON).

Distributed Linkback Graph (DLBG) works based on the following rules:

- The graph consists of Nodes and Links
- Each Node is identified by a URL
- A Node has: one value, an array of links, an array of linkbacks
- Links are typed one-way connections from one Node to another.
- Link types are a special kind of Node
- Nodes can (but are not required to) reciprocate a link through the linkback mechanism.
