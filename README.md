# Algorithm for Finding Numbers Less Than or Equal to K

In this repository, we address the challenge of identifying all numbers within an array that are less than or equal to a user-specified number, K. Our solution is founded on a hybrid approach that combines Grover's quantum search algorithm with a Hash Map-like method for state encoding.

## Hash Function Property

The hash function is designed such that it encodes each array element less than K into a quantum state. While not mandatory, the binary representation of this state is also preferably less than the specified number K. This encoding process is efficient, with an insertion complexity of **O(1)**.

## Algorithm Complexity

The search operation for elements less than K maintains a complexity of **O(√n)**, despite the initial setup complexity of **O(n)**. Consequently, this algorithm achieves a **O(√n)** complexity for standard database operations post-setup.

## Pseudo-code

```plaintext
InitializeQubits() // Prepares qubits with uniform distribution using Hadamard gates and creates the diffusion operator

for element in array do
    code = Encode(element) // Encodes the element into a state and returns it
    if element < k then
        addToOracle(code) // Adds the state to the Grover operator
    end if
end for // Setup completion

Grover() // Applies Grover's algorithm, resulting in a uniform distribution among states with numbers less than k
```
InitializeQubits() // Prepares qubits with uniform distribution using Hadamard gates and creates the diffusion operator

for element in array do
    code = Encode(element) // Encodes the element into a state and returns it
    if element < k then
        addToOracle(code) // Adds the state to the Grover operator
    end if
end for // Setup completion

Grover() // Applies Grover's algorithm, resulting in a uniform distribution among states with numbers less than k
\```

## Visualization

An illustrative example of the algorithm, which searches for all numbers less than or equal to 7, is provided as an image in the repository.

## References

Grover, Lov K., "A fast quantum mechanical algorithm for database search", Proceedings of the 28th Annual ACM Symposium on the Theory of Computing (1996).

