# Caching

- Caching is a technique to store frequently used data in a fast access memory rather than accessing data every time from slow access memory.
- This makes our system very fast.
- It helps to reduce the latency.
- It also helps to achieve the fault tolerance.

There are different types of caching present at different layer of the system Like:

- Client side Caching (Browser Caching)
- CDN (used to store the static data)
- Load Balancer
- Server Side Application Caching (like Redis etc.)
etc.

```mermaid
graph LR
    %% Define Elements
    Client[CLIENT]
    LB[LB]
    AppServer[App<br>Server]
    Cache[Cache<br>Redis]
    DB[(DB)]

    %% Apply Style Classes
    class Client client;
    class LB lb;
    class AppServer app;
    class Cache cache;
    class DB db;

    %% Define Node Styles
    classDef client fill:#2d2d2d,stroke:#ffffff,stroke-width:2px,color:#ffffff;
    classDef lb fill:#2d2d2d,stroke:#ffffff,stroke-width:2px,color:#ffffff;
    classDef app fill:#2d2d2d,stroke:#ffffff,stroke-width:2px,color:#ffffff;
    classDef cache fill:#2d2d2d,stroke:#ffff00,stroke-width:3px,color:#ffff00;
    classDef db fill:#2d2d2d,stroke:#ffffff,stroke-width:2px,color:#ffffff;

    %% Connections
    Client --> LB
    LB --> AppServer
    AppServer --> Cache
    Cache --> DB

    %% Diagram Styling Configuration
    linkStyle default stroke:#ffffff,stroke-width:2px;
```

## Distributed Caching

`Distributed caching` is an architecture that pools the RAM of multiple networked servers to create a single, unified in-memory data store.

It drastically improves application performance and scalability by serving frequently accessed data from memory instead of repeatedly querying slower backend databases.

---

## Strategies

- [Cache Aside](./cache-aside.md)
- [Read Through](./read-through.md)

- [Write Around](./write-around.md)
- [Write Back](./write-back.md)
- [Write Through](./write-through.md)

---

## Cache Evicsion Policies

**Most Common Policies**

`LRU (Least Recently Used)`: Discards the data that has not been accessed for the longest time.

`LFU (Least Frequently Used)`: Discards the data that has been accessed the fewest number of times.

`FIFO (First In, First Out)`: Discards the oldest data entry based on the order it arrived, regardless of how often it was accessed.

`LIFO (Last In, First Out)`: Discards the newest data entry added to the cache.RR (Random Replacement): Randomly selects and discards any candidate item to free up space.

**Time-Based Eviction**

`TTL (Time to Live)`: Automatically expires and removes a data entry after a fixed, predefined duration from its creation or last update.
