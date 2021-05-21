# starve-free-readers-writers

The reader's writers problem arises when multiple processes try to access the same resource. We call the processes trying to read "readers" and those trying to update the resource "writers". The objective is to prevent simultaneous access of the resource by both readers and writers. Doing so while preventing starvation of both readers and writers is the problem we will try to address.

The solution is to place each process trying to access the resource in a first in first out queue. No reader can enter the critical section while a writer process is waiting to access the resource. The reader signals the writer to enter its critical section while the following contidions are met :

- a writer is waiting
- if it was the last reading process

The psuedocode is contained in :
- Semaphore.txt
- Processes.txt
### References

- Operating Systems Concepts (9th Edition), Abraham Silberchatz, Peter B Galvin and Greg Gagne
- [arXiv:1309.4507](https://arxiv.org/abs/1309.4507)
