# Race Condition in Concurrent Counter

This repository demonstrates a common concurrency bug in Java: a race condition.  The `Counter` class attempts to increment a counter, but when used by multiple threads concurrently, it produces an incorrect result. This is because the `increment()` method is not atomic; multiple threads can interfere with each other's updates.

The solution demonstrates how to fix this using the `AtomicInteger` class, which provides atomic increment operations.

## How to Run

1. Clone the repository.
2. Compile and run `Main.java`.
3. Observe that the final count is often less than 2000 due to the race condition.
4. Uncomment the solution in `Main.java`, recompile, and run again. Observe that the count is now consistently 2000.