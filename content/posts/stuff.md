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
acquainted with Hexagonal Architecture. Here, I document my understanding of the
architecture.

## Traditional Architecture

Before going into the details of **hexagonal** architecture, it's useful to take a
quick review of traditional layered architecture and shortcomings associated with
this and why alternative approaches may be preferable. 

In traditional **layered** architecture, also known as n-tier architecture
components are organized into several horizontal layers that function together 
as a single unit of software - a layer is a logical separation of components and
code.

In layered architecture each layer is only connected to the layer directly below
them, but they do not depend on each other, the layers are isolated.

### Example of Layered Architecture

A traditional web application may consist of the following layers:

- Web Layer
- Domain / Business Layer
- Persistence Layer

@TODO: Diagram
  
We receive a web request in the **web layer**, which performs routing and makes calls
to a service existing in the **domain layer**. The service is responsible for
business logic, and making calls to the **persistence layer** to either query for data
or modify the current state of domain entities.

### Advantages of Layered Architecture

Can build layers independent of each other - in the example of a web application
the Domain is separate from the Web and Persistence layer, allowing for them to
be swapped out, without affecting the domain logic.


### Disadvantages of Layered Architecture

Layered architecture is the architecture I am most familiar with, having encountered
it extensively in almost all projects I have worked on, and whilst when
implemented and enforced with discipline, this approach is solid, it was interesting
to read some of the critisms of laeyered architecture, and I was able to identify
scenarios in which boundaries had been breached, and the impact this could have.


```php
```



# Resources

- https://www.baeldung.com/cs/layered-architecture
- 
