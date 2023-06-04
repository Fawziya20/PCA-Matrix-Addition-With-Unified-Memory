# PCA-Matrix-Addition-With-Unified-Memory
Refer to the program sumMatrixGPUManaged.cu. Would removing the memsets below affect 
performance? If you can, check performance with nvprof or nvvp.
## Aim:
The aim of this experiment is to demonstrate matrix addition using CUDA programming with unified memory.

## Procedure:
1. Allocate unified memory for matrices A, B, and C.
2. Initialize matrices A and B with appropriate values.
3. Define the grid and block dimensions for the CUDA kernel.
4. Launch the CUDA kernel to perform matrix addition.
5. Synchronize the device to ensure all CUDA operations are completed.
6. Print the result matrix C.
7. Free the allocated device memory.

## Output:
![240340364-07a8472f-09d2-4601-a9c3-baefbec34321](https://github.com/Fawziya20/PCA-Matrix-Addition-With-Unified-Memory/assets/75235022/e23cb2f8-c779-4fd2-b3f9-aa6549b5f596)


## Result:
The memset function calls are not necessary in this program. They were originally used to set the memory blocks for matrices A, B, and C to zero. However, the subsequent initialization loops already assign specific values to each element of the matrices, overwriting the previous values set by memset. Removing the memset calls does not affect the correctness of the program and has no significant impact on its performance. It is good practice to remove unnecessary code to improve code readability and maintainability.
The result printed to the console, showing the elasped time in the Host and the GPU to compare their performance.
