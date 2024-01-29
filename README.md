# Week 2 Questions

## Three Service Models

| Service Model|Pros  | Cons |
|:-------------|:-----|:-----------|
| ***Infrastructure as a Service (IaaS)*** |  &bull; Provider provisions processing, storage, networks, and other fundamental computing resources.<br> &bull; Consumer can run arbitrary software, which can include operating systems and systems.| &bull; Provider controls the underlying cloud infrastructure.<br>&bull; Consumer must control  the operating system, storage, deployed systems, limited control of select components (host firewalls.)
| ***Platform as a Service (PaaS)***  | &bull; Consumer controls deployed systems and possibly configuration settings for the system-hosting environment.<br> &bull; Provider provides programming languages, libraries, services, and tools. | &bull; Provider controls the underlying cloud infrastructure including network, servers, operating systems, and storage. <br>  &bull; Consumer must deploy consumer-created or acquired systems created using programming languages, libraries, services, or tools supported by the provider. 
| ***Software as a Service (SaaS)***| &bull; Provider supports systems running on a cloud infrastructure. <br> &bull; Consumer uses provider's systems on a cloud infrastructure through a thin client or program interface. | &bull; Provider controls underlying infrastructure including the network, servers, operating systems, storage, or even individual system capabilities. <br> &bull; Consumer controls limited user specific system configuration settings. | 

## Three state solutions
1. *Stateful* service: The history is maintained in the service. If the service goes down, the data is lost. Not an ideal solution for the developer or the user. There are two stateless options:
1. *Stateless* service (option 1): The history is maintained in the client. If the client deletes the data, the data is lost. This is the best solution for personal privacy.
1. *Stateless* service (option 2): The history persists in the database. If the database is corrupted, the data is lost. This is the best solution for storing large amounts of data "in the cloud." 

## Example Application
My bank has "lost" consumer deposits a couple of times ([March 2023](http://archive.today/XBUME) and [August 2023](http://archive.today/QLkmC)) but always regained them within a few hours. I can only speculate exactly what the "technical issue" was, but it is possible that, on both occasions, the leader service instance went down. 

Let's assume the bank kept its data in a cluster that used a distributed coordination system such as Adobe Zookeeper. Each cluster has a service instance that is a *leader* with several other instances that are *followers*. If the follower fails, the cluster creates and populates a new follower rather quickly. However, if the leader service instance fails, it takes longer for the followers to choose a new leader and bring it up-to-date using persistence mechanisms. 

I suspect what I described happened in the following way: The *leader* that had the latest data had to be brought up-to-date. Unfortunately, in the meantime, many of us had accounts overdrawn and resulting fees due to this server outage. I was only affected once, but I had "lost" my yearly company bonus for a few hours, which was upsetting. I seriously contemplated switching banks. Then I discovered that fintech is [highly dependent on legacy systems](http://archive.today/2tLFf), so perhaps it is better that I stay for now until more banks update their systems to have the features I expect from my bank. 
