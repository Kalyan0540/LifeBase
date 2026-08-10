---
source_title: "900+ hours of Learning System Design in 9 Minutes"
source_url: "https://www.youtube.com/watch?v=3Pusamd6BO4"
created: 2026-07-17
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=3Pusamd6BO4)

Try Opera Neon, the AI browser for researching, summarizing docs and working with multiple AI models: https://opr.as/Opera-neon-maddyzhang  
  
Everyone is talking about system design, but to actually crack senior-level interviews, get better offers, or build scalable systems, you need to understand the core principles, not just memorize buzzwords.  
  
In this video, I break down the 6 system design concepts that completely changed how I think about architecture.  
  
Whether you're preparing for system design interviews, trying to level up as a software engineer, or learning how real distributed systems work, this video will help you build the right mental models.  
  
💡 Here’s what you’ll learn:  
✅ Statelessness — why scalable servers should not remember previous requests  
✅ Caching — how systems trade freshness for speed using Redis, CDNs, and browser caches  
✅ CAP Theorem — why distributed systems must choose between consistency and availability  
✅ Message Queues — how Kafka, SQS, and async workflows make systems more resilient  
✅ Databases — when to use SQL vs NoSQL and why ACID guarantees matter  
✅ API Design — how REST, GraphQL, versioning, and contracts shape reliable systems  
  
👋 about me  
I’m Maddy, a senior software engineer (prev. at Google), with prior internships at Amazon, IBM, and Microsoft. Sharing my journey here - thanks for watching 🤍  
  
🔗find me on other socials  
Instagram https://www.instagram.com/madeline.m.zhang/  
LinkedIn https://www.linkedin.com/in/madelinemzhang/  
Tiktok https://www.tiktok.com/@madeline.m.zhang  
  
📖 Timestamp  
0:00 Intro  
0:59 Concept 1  
3:24 Concept 2  
4:22 Concept 3  
5:35 Concept 4  
6:29 Concept 5  
8:17 Concept 6  
9:04 Final Advice  
  
🔔 Subscribe for more coding, system design, DSA, and tech career videos!  
  
\*disclaimer: views are all my own and do not represent any current / past employer(s)  
  
Thank you to Opera Neon for sponsoring this part of the video.  
  
#systemdesign #softwareengineering #codinginterview #systemdesigninterview #seniorengineer #softwaredeveloper #techcareers #backendengineering #distributed systems #scalability #caching #redis #kafka #sqs #captheorem #databases #sql #nosql #acid #apidesign #restapi #graphql #loadbalancing #techjobs #faang #google #amazon #coding #programming #computerscience

## Transcript

### Intro

**0:00** · The gap between a junior engineer and a highly paid senior developer isn't years of experience. It's how you think about systems. Senior engineers get promoted, get better offers, and get higher pay because they can reason about architecture, not just write code. And in this video, I'm going to break down the six concepts that completely change how you will understand system design.

**0:19** · Hi friends, I'm Maddie. \[music\] I'm a senior software engineer who previously worked at Google and internet other big tech companies like Amazon, IBM, and Microsoft. When I first started studying system design, I made the classic mistake. I tried to memorize everything.

**0:32** · DNS, sharding, CDNs, item potency, but I was building just a glossary, not a mental model. So, I could recite definitions, but I couldn't actually reason through a new problem and would freeze during interviews. What completely changed my approach wasn't learning more concepts. It was understanding the why behind them, the principles that tie everything together.

**0:53** · Once that clicked, I stopped blanking interviews and actually started designing systems with confidence. Our first concept is statelessness. Everyone learns horizontal scaling means adding more servers. That is true, but it took me a while to internalize that you can actually really only do that if your servers are stateless. Stateless means the server doesn't remember anything about a previous request. Every request carries everything the server needs to process it, usually via a token that lives on the client side. The server treats every single request like it's meeting you for the very first time. So, why does this matter so much?

### Concept 1

**1:23** · If your server stores session data locally, like a user's login state or an in-progress cart, you can't just route their next segment to any server anymore. That user has to go back to the specific server that remembers them. That's called a sticky session, and it's a real problem.

**1:39** · Your load balancer's hands are tied, your servers aren't actually interchangeable, and if that one server goes down, the session is just gone.

**1:47** · When you offload state to a shared store, like Redis or a distributed cache, suddenly every server is identical. Your load balancer can route freely, you can spin servers up and down without losing data, and you get real fault tolerance. So, before you ask, "How do I scale this?" ask, "What state is each server holding and where should it actually live?" Before we get to the next topic, I want to thank the sponsor of this part of the video, Opera Neon.

**2:11** · If you're studying system design, you know how much of it is just piecing together lots of research, reading docs, comparing approaches, and trying to synthesize a dozen different sources at once. Opera Neon is a browser built to make working with AI actually feel manageable day-to-day. You get access to multiple AI models directly inside the browser, and you can switch between them depending on the task without bouncing between a bunch of separate tools. The workflow I keep coming back to is deep research.

**2:34** · For example, when I was learning about distributed caching, I wanted to compare Redis versus Memcached across latency tradeoffs, eviction strategies, and how each one holds up at scale. Normally, that's 10 tabs and a bunch of context switching. With Neon, I can just run a research session right in the browser, and it then runs a multi-agent parallel investigation to bring information from all my sources, creating an incredibly detailed and in-depth report for me. There are also cards, save shortcuts for tasks you do repeatedly.

**3:01** · I have one set up for summarizing technical documentation, which comes up constantly when I'm trying to quickly understand a new framework, API, or model release without losing the important implementation details. And beyond just the product, Neon has a Discord community where you can share AI workflows with other people and actually shape how the browser evolves. Here, you can get early access to updates and direct conversations with the team building it. It's $20 a month includes access to all of those models in one place. The link to check it out is in the description. All right, let's get back to the concepts. Now, let's talk about our second concept, caching.

### Concept 2

**3:34** · It shows up everywhere in system design, your browser, your CDN, your app server, and your database. And it can feel like a dozen separate things to learn. But every cache is essentially making the same tradeoff, speed in exchange for freshness. You're storing a copy of data somewhere faster and closer to where it's needed, and accepting that the copy might be slightly out of date. When that clicked for me, I stopped memorizing when to use Redis or CDN versus browser cache, and instead started asking things like where's the bottleneck and how stale can we afford the data to be.

**4:02** · CDNs serve static content close to users geographically and are great for assets that change rarely. Application-level caches like Redis sit in front of your database and are great for read-heavy queries where you need millisecond latency. And database query caches live inside the database itself. So, make sure you get comfortable with concepts like TTLs, cache-aside patterns, and write-throughs versus write-back strategies. Understanding these three things will cover the vast majority of caching questions in interviews. Concept three is CAP theorem.

### Concept 3

**4:31** · Most people learn CAP theorem as you can only have two out of the three of consistency, availability, and partition tolerance.

**4:40** · But, in reality, partition tolerance isn't optional. In any real distributed system running over a network, partitions will happen. Nodes will lose connectivity and packets will drop. So, partition tolerance is essentially a given constraint. It's not a choice.

**4:55** · What you're actually choosing between is now consistency and availability.

**4:58** · Consistency means every read gets the most recent write. So, if I update my profile, anyone who reads it right after sees the updated version. Availability means the system always responds even if it can't guarantee it's the very latest data. But, for all practical intents and purposes, most systems don't need to make this choice globally. Different parts of the same system can make different decisions. At Google, there were services where strong consistency was completely non-negotiable: financial transactions, access control, and permissions. And there were other features where eventual consistency was totally fine, like content feeds.

**5:30** · So, in a system design interview, don't just say, "I'll go with eventual consistency." Instead, explain which specific operations need which guarantees and why. Concept four is message queues. Let's say a user places an order. In a synchronous world, that means this: Place order, call the inventory service, call the payment service, call the notification service, all in real time, all before the user gets a response. However, in this scenario, you've created a chain of dependencies. If the notification service is slow or temporarily down, the entire order flow fails.

### Concept 4

**6:01** · Your system's end-to-end reliability is now the product of every dependency's uptime.

**6:07** · Message queues break that dependency.

**6:09** · Instead of calling services directly, you publish an event like order placed.

**6:13** · Something like Kafka or SQS holds that event. Each downstream service, inventory, payment, notifications, picks it up and processes it independently on its own schedule. The result is that your services are resilient to each other's failures. If the notification service goes down, the message just waits in the queue and gets processed when it comes back up. The order still goes through. Concept five is databases.

### Concept 5

**6:36** · The SQL versus NoSQL debate gets framed as if it's about old versus new or simple versus scalable, but it's really not. It's about what guarantees your data layer needs to make. SQL databases are built around a concept called ACID: atomicity, consistency, isolation, and durability. These four properties are worth actually knowing instead of just recognizing this acronym. Atomicity means a transaction is all or nothing.

**7:02** · If you're transferring money between two accounts, debiting one and crediting the other, either both operations succeed or neither does. You never want to end up in a state where the money left one account but didn't arrive in the other.

**7:13** · Consistency means the database always moves from one valid state to another.

**7:16** · Your schema constraints, foreign keys, and rules are always enforced, and you can't write data that violates them.

**7:23** · Isolation means concurrent transactions don't interfere with each other. So, two users hitting the database at the same time see a clean, predictable result as if the transactions ran one after another. And durability means once a transaction is committed, it stays committed even if the server crashes right after. It's on disk and permanent.

**7:41** · NoSQL databases, on the other hand, trade some of these guarantees for scale and flexibility. They drop the strict schema, often relax consistency, and that's specifically what lets them scale horizontally across many machines so easily. That trade-off is a feature and can be great for the right use case. So, the actual question here isn't if we should use SQL versus NoSQL. It's does my application need ACID guarantees?

**8:03** · Things like financial transactions, inventory systems, anything where partial rights are catastrophic that you would use SQL for. Use your activity feeds, product catalogs, real-time analytics at massive scale where slightly stale data is fine means that you can often use NoSQL. A lot of real production systems usually use both with each handling the part of the workload it's suited for. And last but not least, let's talk about API design. Your API is a contract with every client that depends on it. Once you ship it, changing it isn't a code update. It's a coordinated migration affecting everyone downstream.

### Concept 6

**8:33** · Now, let's talk about REST versus GraphQL. They optimize for different things. REST is simple, cacheable, and easy to reason about and is great for things like public APIs, mobile clients, and teams that need a stable, well-documented interface.

**8:47** · GraphQL is flexible and lets clients request exactly what they need, which is great when you have many clients with different data needs like a web app and a mobile app hitting the same back-end.

**8:57** · But regardless of which approach you choose, the principle of good API designs are the same. Be explicit about versioning from day one. Design endpoints around resources, not internal operations, and document your contracts before someone else has to reverse engineer them. In conclusion, those were the six concepts that made system design click for me. If you're actively preparing for system design interviews right now, my advice is to take one of these concepts at a time and apply it to a real system used daily. So, for example, how does Spotify use caching across different layers?

### Final Advice

**9:26** · When does Venmo need strong consistency versus when can it relax? And that's all I have for you in this video. If you want more content on systems, technical interviews, and navigating a career in software engineering, give this a like, hype the video, and subscribe. Thanks for watching, and I'll see you next one.