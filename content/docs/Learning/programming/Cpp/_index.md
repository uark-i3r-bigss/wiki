---
title: C++
---

# The STL Library

STL is a library of C++ template classes to provide common programming data structures and functions. STL has 4 major components:

* Containers
* Iterators
* Algorithms
* Function Objects

## Containers

### Sequence Containers

<img src="sequential_containers.png" alt="Sequential Containers" style="width:85%;"/>

### Associative Containers

<img src="associative_containers.png" alt="Associative Containers" style="width:95%;"/>

### Unordered Containers

Unordered containers lack an order thus can be visualized as a bag filled with elements. Unordered elements use a hash function to map keys with their values.

<img src="unordered_associative_containers.png" alt="Unordered Associative Containers" style="width:95%;"/>

### Container Adaptors

Container adaptors acts as an interface to provide functionality to pre-existing containers. They are implemented as a wrapper around another container.

<img src="container_adaptors.png" alt="Container Adaptors" style="width:95%;"/>

## Array