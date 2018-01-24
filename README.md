# storloc
A simple memory storage allocator ;)

## Notes
### malloc()
In 32-bit memory, malloc() always returns a pointer to a block of size divisible by 8.
In 64-bit memory, malloc() always returns a pointer to a block of size divisible by 16.

This function can allocate heap memory by using `mmap` function, or it can use the `sbrk` function (which moves the `brk` pointer maintained by the kernel and returns the old value of the pointer).
