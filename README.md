
# Distributed Computing with Grid
## - large-scale distributed high-throughput computing using home computers and other resources.

 Grid computing has brought about a major shift in how we think about how to maximize the value of computing resources. The technology is still in its early stages, but the Grid Computing zone will continue to add new articles, tutorials, resources, and tools to help developers get up to speed on this important technology.

People who are interested in grid computing are asking some very basic questions:

### How do I use all this information?

### How do I combine all this information?

### What’s next?

#### In this chapter, you’ll learn about the great benefits of grid computing. It focuses on the fundamentals of grid computing, and it’s explained through articles, tutorials and tips, IBM training programs, workshops, and IBM products. It’s a simple, easy-to-understand introduction to grid computing, but it also covers the most important points.

The grid isn’t done yet, and grid technology is evolving rapidly. Standards, frameworks, implementations, and applications are constantly changing. Today, grid computing reminds us of the early days of the Web. It started slowly. The same was true with the advent of XML and Web services. However, once solid standards and tools emerge and mature, we can expect tremendous gains and growth in the world of grid computing.

### What is grid computing?

Since grid is a new technology, it can mean many different things to different people, but the concept of grid computing is clearly defined as follows: Grid computing is the integration of servers, storage systems, and networks into a single large system, delivering multi-system resources to individual users. For users, data files, or applications, the system becomes a single, large virtual computing environment.

Grid computing is the logical next step in distributed networking. Just as the Internet allowed people to share ideas and files on a project-by-project basis, grid computing allows people to share the resources of distributed computer systems to do real work on those projects. Grid computing is a device that allows computers (and users) to communicate at a deeper level. Grid computing allows them to use the computing or storage resources of other machines.

In grid computing, organizations transform their distributed, hard-to-manage systems into one large virtual computer, creating complex problems and processes that cannot be handled efficiently by a single computer. The problems addressed can involve data processing, network bandwidth, and data storage. Systems connected to the grid can be co-located or distributed across the globe. They can be a variety of operating systems running on many hardware platforms. They can be owned by different organizations. Regardless of the depth of the grid’s resources, all grid users can experience the resources of a very large virtual computer.

The primary purpose of the grid is to virtualize resources to solve problems. The primary resources of grid computing are many, but this chapter will limit them to:

  - Computing/processing power
  - Data storage/network file systems
  - Communication and bandwidth
  - Application software
    
Since the concept of applying the grid to real life is still new, another way to describe the grid is to identify what the grid is not. The following are not grids:

  - Clusters
  - Network-attached storage devices
  - Scientific instruments
  - Networks
Each of these are important components of the grid, but they are not grids.

So what is needed to bring the concept of grid computing to reality? Standards, fully open, common protocols and interfaces are needed. All of this is currently defined and is similar to making information accessible on the Web.

### Why Grid Computing Matters
Grid computing is about getting computers to work together. In almost every organization, there is a lot of computing capacity that is widely distributed and unused. A UNIX server is actually only running about 10% of the time. Most PCs are doing nothing 95% of the time. Imagine an airline with 90% of its planes on the ground. Imagine an automaker with 40% of its parts plants idle. Imagine a hotel with 95% of its rooms empty.

Virtualization of computing environments—or grid computing—is a key element of IBM’s on demand strategy. Virtualization allows organizations to:

Accelerate business processes by using idle computer resources.
Speed ​​up applications to reduce processing time.
Facilitate the development of new, more productive applications.
Reduce the cost of developing new applications.
Increase collaboration and productivity capabilities.
Maximize the resources available to users.
Increase the resiliency and usability of the IT environment. Here’s why managers and developers benefit from grid computing:

Balancing workloads to optimize infrastructure and provide redundant capacity for demanding applications.
Increasing access to data and supporting collaboration across education, organizations, and businesses.
Providing a more resilient infrastructure.
Businesses benefit from grid computing:

Providing users with the resources they need on demand, increasing productivity.
Using existing resources more efficiently.
Responding quickly to changing business and market demands.
Enables collaboration across distributed entities.
Creates virtual organizations that can share resources and data.
One of the most important issues grid computing brings to businesses is the utilization of existing resources. Businesses have invested heavily in computing capacity, but more than 90 percent of it is sitting idle. With grid computing, businesses can connect unused assets, harness their collective power, and manage them as one big computer.

### How do you use grid computing?
The concept of grid computing originated in research and academic communities. Similar to the Internet, businesses are using grid computing for new types of financial and business models.

In the financial services sector, grid computing can speed up transactions, break down huge amounts of data, and provide a more stable IT environment in mission-critical environments.
Government agencies can use grids to pool, secure, and integrate huge amounts of data. Many civilian and military agencies require cross-agency collaboration, data integrity and security, and fast access to information.
Companies in the life sciences sector, which conduct genomic research and develop medicines, can use parallel grid computing to process and compare huge amounts of data. Faster processing means faster time to market, which is a critical factor.
These new grid-oriented business models can be implemented, and some have already been implemented.

### Core Components of Grid Computing
Grid computing has six main components:


  - Security
  - User Interface
  - Workload Management
  - Scheduler
  - Data Management
  - Resource Management
Let’s take a closer look at each one.

Computers on the grid are networked and run applications. Because they process sensitive or highly valuable data, the security aspects of grid computing are very important. These include encryption, authentication, and authorization.

Accessing information on the grid is also very important, and the user interface component does this. It takes one of two approaches:

The interface provided by the application the user is running.

The interface provided by the grid manager, which is like a web portal that accesses applications and resources running on the grid in a single virtual space.

The portal-style interface is also important, because it provides a place for the user to learn how to query the grid.

The applications that the user is running on the grid need to know what resources are available. This makes the workload management service easier. The application can communicate with the workload manager to discover available resources and their status.

The scheduler is needed to place computers where the application will run and assign tasks. It can be as simple as acquiring resources that are available in the future, but it also needs to determine the order of tasks, manage the load, find solutions when resources are available, and monitor the process.

If an application is running on a system that does not have the data it needs, a secure data management device will move the data to the right place.

A resource management device is needed to handle the core tasks of starting a job with specific resources, monitoring the status of the job, and inspecting the results.

Grid computing does not operate in a vacuum. Rather, all protocols and computer technologies are potentially involved. Therefore, to fully understand the scope of grid computing's power, you need to understand other technologies and standards as well.

### Grid Computing and Standards
To understand grid computing standards, you also need to understand how grid architecture is defined. Let's look at the architecture definition of the Open Grid Services Architecture (OGSA) developed by members of the Global Grid Forum (GGF).

Architecture -- OGSA defines what a grid service is, the overall structure and services provided in a grid environment. Based on existing web service standards, OGSA defines grid services as web services that conform to specific conventions. For example, grid services are defined in terms of the standard Web Services Definition Language (WSDL).

Why is this important? It provides a common open standards-based technology that allows access to a variety of grid services using existing standards such as SOAP, XML, and WS-Security. Additional services can be added or integrated based on this.


It also provides a standard way to discover, define, and leverage new grid services.

OGSA also provides interoperability between grids implemented using a variety of tools.

Specifications -- Grid specifications are evolving. Organizations such as GGF and OASIS are defining grid standards in areas such as:

  - Applications and programming practices
  - Architecture
  - Data management
  - Security
  - Performance
  - Scheduling and resource management
The Open Grid Services Infrastructure (OGSI) is the official specification for the concepts described by OGSA, but has been superseded by the Web Services Resource Framework (WSRF). The goal of WSRF is to evolve grid architecture in the manner of Web services. Instead of defining new types of grid services, this specification requires that services defined by OGSA rely entirely on standard Web services.

How much do you need to know about the evolution of grid standards? It depends. IBM and various software researchers are defining grid standards. Are you a software developer at an enterprise? If so, you will be using grid tools and products based on new standards. Keep an eye on the standards and how they are progressing.

### Grid Implementation
Grids can be implemented using open source and commercial tools and products. As grid standards become more established, vendors are demanding components that are compliant and easy to combine.

What are the basic technologies required to implement a grid? What are the essential services for grid computing? The services are:

  - Data query
  - Data management
  - Processor requests
  - Workload balancing
  - Job scheduling
  - Bandwidth allocation
These services are called grid services. Some computers host grid services, and some computers run applications that have contracted with grid services as clients. Grid services are essentially web services with additional functionality.

Web services—groups of application functionality that can be called over a network—allow applications to communicate with each other, regardless of platform or programming language.

Tools are needed to implement a grid. The following categories of grid tools are provided:

Infrastructure components include file systems, schedulers and resource managers, messaging systems, security applications, authentication, and file transfer mechanisms (GridFTP).

Systems on the grid must be able to find services that they can use. In order to share and collaborate, the topology of the grid needs to be defined and monitored. For this purpose, there are grid directory service implementations based on existing models such as LDAP, DNS, network management protocols, and indexing services.
One of the main advantages of grids is their increased efficiency. This is possible because of the scheduler and load balancer. The scheduler ensures that tasks are completed in a specific order, and the load balancer distributes tasks and data management across systems to reduce bottlenecks.
Tools for grid developers focus on a variety of purposes (file transfer, communication, environmental control) and range from utilities to APIs.
Security in a grid environment means authentication and authorization, but also important issues such as message integrity and confidentiality.
A good starting point for implementing a grid is to download the Globus Toolkit. This toolkit, developed by the Globus Project, is a set of services and software libraries designed to support grids and grid applications.

The Commodity Grid Kit (CoG) provides access to grid services through specific frameworks such as Java, Python, and Perl.

  - Applications for the grid
  - This part requires some planning.

You need to think about the basic structure that will provide the grid and services. You need to think about how to fit together infrastructure components such as security, resource management, information services, and data management that will affect application architecture, design, and deployment.
