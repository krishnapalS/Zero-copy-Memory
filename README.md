# Zero-copy-Memory

We will attempt to use Zero-Copy approach, which uses mapped memory. The memory needs, again, to be pinned on the host, either with cudaHostAlloc or using cudaHostRegister (this time with cudaHostRegisterMapped flag). Next we will need to acquire device pointer which would refer the same memory with cudaHostGetDevicePointer and no explicit copying will be needed. The resulting code definitely looks simpler.
