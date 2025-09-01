# What is Scalability

Scalability is an ability to adjust the capacity of the system to cost efficiently fulfill the demands.
It usually means an ability to handle more users, clients, data, transactions or requests without affecting the user experience.

Most scalability issues can be boiled down to just a few measurements.

-   Handling more data:

    -   more user accounts
    -   more products
    -   more location data
    -   more pieces of digital content

    Processing more data puts pressure on your system, as data needs to be sorted, searched, read from the disks, written to disks, and sent over the network.

-   Handling higher concurrency levels:

    -   Concurrency measures how many clients your system can serve at the same time.
    -   Concurrency is difficult, as your servers have a limited amount of CPUs and execution thread.
    -   Higher concurrency means more open connections, more active threads and more messages being processed.

-   Handling higher interaction rates
    -   It is related to concurrency but is slightly different dimension.
    -   The rate of interaction measures how often your clients exchange information with your servers.
    -   Examples:
        -   If you are building a website, your clients would navigate from page to page every 15-120 seconds.
        -   If you are building a multiplayer mobile game, you may need to exchange messages multiple times per second.
        -   The main challenge related to the interaction rate is **latency**

As you noticed, scalability is related to perfomance, but it is not the same.

-   **Perfomance** measures how long it takes to process a request or perform a certain task.
-   **Scalability** measures how much we can grow.

For example, if you had 100 concurrent users, with each user sending a request, on average, once every 5 seconds, you would end up with a _Throughput_ requirement of 20 requests per second.
_Perfomance_ would decide how much time you need to serve these 20 requests per second, and _scalability_ would decide how many more users you can handle.
