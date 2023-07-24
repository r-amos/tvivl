---
title: 'Hexagonal Architecture: Part One'
summary: >
    An exploration of hexagonal architecture.
date: 2023-02-04T22:08:41Z
draft: false
slug: hexagonal architecture part one
---

## Introduction

For educational purposes, I recently started writing an web application in node.js 
with the Express framework. Coming from a PHP background and having used Laravel 
extensively on both professional and personal endeavors, I had the opportunity 
to think about the architecture of the application a bit more, and as such became
acquainted with Hexagonal Architecture. Here, I document *my* understanding of the
architecture, along with a number of side quests and rabbit holes I went down along
the journey.****

## Traditional Architecture

Before going into the details of **hexagonal** architecture, it's useful to take a
quick review of traditional layered architecture and any shortcomings associated with
this and why alternative approaches may be preferable. There are numerous
architecture patterns, but layered is the one I've encountered the most and feel
hexagonal attempts to improve upon.

In traditional **layered** architecture, also known as **n-tier** architecture
components are organized into several horizontal layers that function together 
as a single unit of software. A layer is a logical separation of components and
code, and has a specific role and responsibility within the application. Components
within a layer only handle logic relevant to that layer, maintaining a separation
of concerns between components.

@TODO: Layered Diagram

Each layer can be either open or closed. When closed, a layer can only access 
the layer directly below them to prevent developing tight coupling between layers,
as a request is received it must travel through all the layers

### Example of Layered Architecture

A traditional web application may consist of the following layers:

- Web Layer
- Domain / Business Layer
- Persistence **Layer**

@TODO: Diagram
  
We receive a web request in the **web layer**, which performs routing and makes calls
to a service existing in the **domain layer**. The service is responsible for
business logic, and making calls to the **persistence layer** to either query for data
or modify the current state of domain entities.

### Advantages of Layered Architecture

Can build layers independent of each other, due to the separation of concerns
between components - in the example of a web application the Domain is separate 
from the Web and Persistence layer, allowing for them to be swapped out without 
affecting the domain logic.


### Disadvantages of Layered Architecture

Layered architecture is the architecture I am most familiar with, having encountered
it extensively in almost all projects I have worked on, and whilst when
implemented and enforced with discipline, this approach is solid, it was interesting
to read some of the criticisms of layered architecture, and I was able to identify
scenarios in which boundaries had been breached, and the impact this could have.


```php
```

# Summary

So, there it is, a bunch of theory around hexagonal architecture.

# Resources

- https://www.baeldung.com/cs/layered-architecture
- 
