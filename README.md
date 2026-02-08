# Java-Pep-(mini)PROJECT-# Command-Driven In-Memory Database

This project implements a thread-safe in-memory key-value database
with TTL support and concurrent command execution.

 Features-

- Integer key storage
- TTL expiration
- Lazy expiration on GET
- Background cleaner thread
- Thread-safe using ConcurrentHashMap
- Lifecycle control (START / STOP)
- Custom exception handling
- Multi-threaded demo

 OOP Design - 

- Command parsing separated from DB logic
- Entry class encapsulates value + expiry
- Database class manages concurrency
- Cleaner thread runs independently

 Thread Safety Strategy-

ConcurrentHashMap ensures safe concurrent access
without global locks.

Volatile flag guarantees visibility of DB state
between threads.

Cleaner thread safely removes expired keys
during iteration.

How to Run - 

Compile:

javac Main.java

Run:

java Main
