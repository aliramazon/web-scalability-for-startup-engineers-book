# Making Server Stronger

Once your application reaches the limit of your server (due to increase in traffic, amount of data processed, or concurrency levels), you must decide how to scale.

There are two types of scaling:

1. Vertical
2. Horizontal.

## Vertical Scalability

_Vertical scalability_ is accomplished by upgrading the **hardaware** and/or **network throughput**. It is often the simplest solutuon for short term scalability as it does not require architectural changes to your application.

There are a number of ways to scale vertically:

-   Addning more I/O capacity by adding more hard drives in Redundant Array of Independent Disks (RAID) arrays. I/O throughput and disk saturation are main bottlenecks in database servers.
-   Imrove I/O access times by switching to solid-state drives (SSDs). Random reads and writes using SSDs are between 10 and 100 times faster.
-   Reducing I/O operations by increasing RAM. Adding more memory means more space for the file system cache and more working memory for applications.
    When you increase RAM, the system can store more data in memory instead of constantly reading from and writing to storage devices (SSDs/HDDs), which are much slower than RAM.
-   Improving **network throughput** by upgrading network interfaces or installing new ones. **A network interface** is the hardware component that allows a computer or device to connect to and communicate with a network.
-   Switching to servers with more processors or more virtual cores(12 or 24).

Vertical scalability comes with some serious limitations:

-   First one being cost.
-   The second one is that it actually has hard limits. No matter how much money you may be willing to spend, it is not possible to add memory. Simply put, at a certain point, no hardware is available that could support further growth.
