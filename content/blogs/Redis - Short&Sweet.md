---
title: Redis - Short&Sweet
type: page
# description: Click on me to see the content.
topic: career
author: Noble Varghese
---

## 🔎 What is redis?
Redis(REmote Dictionary Service) is a key-value database server. It can be used as an in-memory datastore, cache and a message broker. It's open-sourced and gained its popularity for its speed, versatility and scalability.

## 🧐 Why do we use Redis?

Primarily it is used as an in-memory cache placed in-front of the actual database like MySQL.
These are used to access data that are changed infrequently and are accessed often. Having a cache improves the application performance as it reduces the load on the actual database.
It's easier to manage data in redis as they're stored as data-structures and supports a wide range of formats like strings, lists, sets, hashes, and sorted sets.
It is fast, scalable and relatively easy to maintain.

## 🛠️ How does Redis work?

Redis works by storing the data in-memory unlike the traditional database that stores on disk making it faster than the disk-based database as it avoids a trip to the disk.

Redis employs a primary-replica architecture and supports asynchronous replication where data can be replicated to multiple replica servers. This provides improved read performance (as requests can be split among the servers) and faster recovery when the primary server experiences an outage. 

Redis comes with point in time snapshots for disaster recovery.

🚀 Redis is an efficient and versatile data management tool that provides fast performance and scalability. It's ideal for various applications such as web applications, messaging systems, and background processing pipelines, helping you achieve your objectives seamlessly.

Credit to: [Youssef Benihoud](https://www.linkedin.com/in/ACoAAEG5tycBZiznaVdUQiOv1BLYM76HVKj6aiE) for awesome diagram

![Alt text](https://noble-varghese.github.io/portfolio/images/redis.jpeg "Redis Architecture Diagram")