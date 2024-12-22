# malloc-c

## Overview
`malloc-c` is a custom implementation of the `malloc` function, a cornerstone of dynamic memory allocation in the C programming language. This project aims to provide an educational understanding of how dynamic memory allocation works under the hood by simulating the behavior of `malloc` and related functions such as `free` and `realloc`.

## Features
- **Custom Memory Management**: Allocate and manage memory dynamically without relying on standard library implementations.
- **Implementation of `malloc`**: Allocate a specified amount of memory from a custom memory pool.
- **Implementation of `free`**: Release allocated memory back to the custom memory pool.
- **Implementation of `realloc`**: Resize previously allocated memory blocks.
- **Memory Pool Simulation**: Manage a pre-allocated memory buffer to simulate the system’s heap.
- **Error Handling**: Handle cases like memory exhaustion or invalid free operations gracefully.

## Prerequisites
To build and run this project, you will need:
- A C compiler such as GCC or Clang.
- A Unix-like operating system (Linux or macOS) or Windows with a compatible development environment.

## Getting Started

### Cloning the Repository
```bash
git clone https://github.com/0xRavenspar/malloc-c.git
cd malloc-c
```

### Building the Project
Run the provided `Makefile` to compile the project:
```bash
make
```
This will generate an executable named `malloc-c`.

### Running the Examples
You can run the examples provided in the `examples` directory:
```bash
./malloc-c examples/example1.c
```

## Usage
### Example: Allocating and Freeing Memory
Here is a basic example to demonstrate the usage of the custom `malloc` and `free` functions:

```c
#include "malloc.h"
#include <stdio.h>

int main() {
    // Allocate memory for an integer
    int *ptr = (int *) my_malloc(sizeof(int));
    if (ptr == NULL) {
        fprintf(stderr, "Memory allocation failed!\n");
        return 1;
    }

    // Use the allocated memory
    *ptr = 42;
    printf("Value: %d\n", *ptr);

    // Free the allocated memory
    my_free(ptr);

    return 0;
}
```

## Contributing
Contributions are welcome! If you find a bug or have an idea for an enhancement, feel free to open an issue or submit a pull request.

### Contribution Guidelines
1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Write clear commit messages and include tests if applicable.
4. Open a pull request with a detailed description of your changes.

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.



