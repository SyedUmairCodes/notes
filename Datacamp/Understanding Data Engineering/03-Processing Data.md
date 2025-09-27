# Processing Data

Data processing is the conversion of raw, unorganized data into meaningful, high-quality, and usable information. 

Not all collected data is perpetually needed. Old or redundant data can be discarded to save storage and processing costs. Additionally, uncompressed data can be significantly larger than compressed data, making compression a vital processing step to avoid prohibitive business costs, especially for large-scale operations. 

Data often needs to be converted from one format to another to be more efficient or suitable for specific uses. Data needs to be moved and organized in a structured manner so that analysts can easily find and utilize what they need.

Processing ensures that data conforms to a predefined schema or structure, allowing organizations to leverage the benefits of structured data. Automating data preparation steps allows data scientists to receive data that is almost immediately ready for analysis. This frees them to focus on deriving insights, which is where they add the most value to the company.

Data engineers play a multifaceted role in data processing, focusing on tasks that are automatable, consistently necessary, and foundational for downstream data users.

-  They automate tasks like rejecting corrupt data and establishing policies for handling missing data.
- They ensure data is stored in logically structured databases and create views on top of existing database tables. 
- Data engineers optimize database performance, Indexing makes data retrieval much faster by creating efficient lookup structures, similar to an index in a book.

>[!NOTE]
>A view is essentially the output of a stored query, combining data from multiple tables for easier access by analysts.

---
## Scheduling Data

Scheduling is a critical component that orchestrates and organizes various tasks within a data engineering system. It ensures that tasks run in a specific order and that all dependencies are correctly resolved, effectively acting as the "glue" that holds the data pipeline together. While scheduling applies to all data processing tasks, this lesson uses the example of updating tables and databases for clarity.

There are different ways to execute tasks within a data pipeline:

- Tasks can be triggered manually, such as an immediate update to an employee table when an employee changes offices.
- Tasks are set to execute automatically based on predefined times or conditions.
	- Running a task at a specific time.
    * Executing a task only when a specific condition is met.
- Manual and automated systems can work in conjunction.

The way data is ingested also influences scheduling:

- Data is collected and sent in batches at specific intervals. Can be cheaper if scheduled during off-peak hours
- Individual data records are sent through the pipeline as soon as they are updated or generated. Provides real-time or near real-time data availability, crucial for immediate user experience.

>[!NOTE]
>While "real-time" is a distinct category, for simplicity, streaming is largely considered synonymous with real-time due to its immediacy in most applications, such as fraud detection.

---
## Parallel Computing

Parallel computing is a core principle underlying almost all modern data processing tools, driven primarily by the need to manage large datasets within memory constraints and leverage increased processing power. In big data processing, a large task is broken down into several smaller, independent subtasks, which are then distributed and executed simultaneously across multiple computers.

- By distributing subtasks across multiple processing units (computers), the overall computational power applied to the problem is significantly increased, leading to faster completion times for large tasks.
- Instead of requiring a single computer to load the entire massive dataset into its memory, parallel computing allows the data to be partitioned into subsets. Each subset is then loaded into the memory of a different computer, resulting in a much smaller memory footprint per individual machine.

While powerful, parallel computing is not without its trade-offs:

- Moving data between different computers in a distributed system incurs a cost, both in terms of time and network resources.
- Splitting a task into subtasks and then merging their results back into a single final output requires communication and coordination between the different processing units. This inter-process communication takes additional time.
- If the performance gains from parallelization are minimal the additional complexity and time incurred by data movement and communication might not be worthwhile.
---
## Cloud Computing

Traditionally, companies processed data in their own on-premises data centers, requiring them to purchase, house, power, and maintain racks of servers. This approach presented several challenges:

- Significant capital expenditure for hardware, ongoing electricity bills, and maintenance costs.
- Processing power often had to be provisioned for peak demand, leading to substantial unused resources during quieter periods.
- Moving offices meant transporting sensitive servers without service interruption.
- To serve a global customer base effectively with low latency, companies would need to establish and maintain data centers worldwide.
- Protecting data from disasters like fires required costly replication of data at geographically distant locations.
    
Cloud computing emerged as a solution to these problems. In the cloud model, companies rent servers and other computing resources from specialized providers.

- No need to purchase and maintain hardware.
- Companies only pay for the resources they use, when they use them, eliminating waste from underutilized capacity. 
- Easily scale resources up or down to meet fluctuating demand, without managing physical infrastructure.
- Cloud providers have data centers worldwide, enabling companies to host applications closer to their global users, reducing latency.
- Cloud providers offer robust infrastructure with built-in redundancy and disaster recovery capabilities across different geographical locations, mitigating risks like data center outages.
- Cloud providers specialize in managing these complex infrastructures, handling security, maintenance, and big data challenges.

The three dominant players in the public cloud market, in order of market share, are AWS, Azure, and Google Cloud. Each provider offers comparable services for core functionalities:

| Service Category | AWS | Azure            | Google Cloud   |
| ---------------- | --- | ---------------- | -------------- |
| **File Storage** | S3  | Blob Storage     | Cloud Storage  |
| **Computation**  | EC2 | Virtual Machines | Compute Engine |
| **Databases**    | RDS | SQL Database     | Cloud SQL      |

While convenient to use services from a single provider, companies can also adopt a multi-cloud strategy, using services from several cloud providers.

**Advantages of Multi-Cloud:**
- Less reliance on a single provider, offering more flexibility and negotiation power.
- Potentially leverage different providers' pricing models for specific services to optimize overall costs.
- May be necessary to comply with data residency or other local regulations that vary by region and provider.
- Provides redundancy against outages of a single cloud provider.

**Disadvantages of Multi-Cloud:**
- Cloud providers actively integrate their services to encourage exclusive use, which can make it challenging to mix and match.
- Services from different providers may not be fully compatible, leading to integration challenges.
- Managing security and governance across multiple cloud environments becomes significantly harder.

----