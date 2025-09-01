# Isolation of Services

Vertically scalability is not the only option at this eary state of evolution. Another simple solution is moving different parts of the system to separate physical servers by installing each type of services on a separate physical machine.

In this context, a service is an application like a web server (for example, Apache) or database engine (for example, MySQL). This gives your web server and database a separate, dedicated machine.

In the same manner, you can deploy other services like File Transfer Protocol, DNS, cache, and others, each on a dedicated physical machine.

> Cache is server/service focused on reducing the latency and resources needed to generate the result by serving previously generated content. Caching is a very important teachnique for scalability. We will discuss it in detail in Chapter 6.

> The core concept behind isolation of services is that you should try to split your monolithic web application into a set of distinct functional parts and host them independently. It is called **functional partitioning**

```mermaid
flowchart TD
    subgraph CLIENT[Client Side]
        C1[Customers]
        C2[Customers]
        C3[Customers]
        C4[Customers]
    end

    subgraph DATACENTER[Data Center]
        WEB[Web Server<br/>Apache]
        DB[Database<br/>MySQL]
        CACHE[Cache Server]
        FTP[FTP Server]
    end

    DNS[DNS Server]

    CLIENT -.->|DNS| DNS
    CLIENT -->|Requests| WEB
    WEB --> DB
    WEB --> CACHE
    CLIENT --> FTP

    %% Styling
    classDef client fill:#e3f2fd,stroke:#1976d2,stroke-width:2px;
    classDef datacenter fill:#f3e5f5,stroke:#7b1fa2,stroke-width:2px;
    classDef server fill:#fff,stroke:#333,stroke-width:1px;

    class CLIENT client;
    class DATACENTER datacenter;
    class WEB,DB,CACHE,FTP,DNS server;
```
