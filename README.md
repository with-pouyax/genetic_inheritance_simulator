# Genetic Inheritance Simulator: Blood Type Edition

## Overview

The **Genetic Inheritance Simulator** is a C program designed to model and visualize the inheritance of blood types across multiple generations within a family tree. By simulating how blood type alleles are passed from parents to offspring, this program provides a clear and interactive way to understand the fundamentals of genetic inheritance.

## Purpose

Understanding genetic inheritance is crucial in fields like biology, medicine, and genetics. This program serves as an educational tool to demonstrate how blood type alleles (`A`, `B`, and `O`) are inherited from parents to children. By simulating multiple generations, users can observe patterns and outcomes of allele combinations, fostering a deeper comprehension of genetic principles.

## Features

- **Family Tree Generation:** Create a family tree spanning a specified number of generations, with each individual represented by their blood type alleles.
- **Random Allele Assignment:** The oldest generation receives randomly assigned blood type alleles, mimicking natural genetic variation.
- **Allele Inheritance:** Subsequent generations inherit one allele from each parent, determining their blood type based on genetic rules.
- **Memory Management:** Efficiently allocates and frees memory for family members to ensure optimal performance and prevent memory leaks.
- **User-Friendly Output:** Displays the family tree with clear indentation and labeling, making it easy to trace lineage and blood type inheritance.

## How It Works

1. **Family Creation (`create_family`):**
   - **Generations > 1:** Recursively creates parent `person` structures for the current individual. Each parent is assigned alleles inherited from their own parents.
   - **Generations = 1:** Assigns random alleles to individuals without parents, representing the oldest generation in the family tree.

2. **Allele Inheritance:**
   - Each child inherits one allele from each parent. The program randomly selects which allele from each parent contributes to the child's genotype.

3. **Family Tree Display (`print_family`):**
   - Prints the family tree with appropriate indentation to represent generational depth.
   - Labels each individual as Child, Parent, Grandparent, etc., based on their generation level.

4. **Memory Cleanup (`free_family`):**
   - Recursively frees memory allocated for each family member to ensure no memory leaks occur.

## Getting Started

### Prerequisites

- **C Compiler:** Ensure you have a C compiler installed (e.g., `gcc`).

### Installation

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/yourusername/genetic_inheritance_simulator.git
   ```
   
2. **Navigate to the Directory:**
   ```bash
   cd genetic_inheritance_simulator
   ```

### Compilation

Use `gcc` to compile the program:

```bash
gcc -o inheritance_inheritance.c
```

### Execution

Run the compiled program:

```bash
./inheritance
```

Upon execution, the program will display a family tree with blood types assigned to each member across the specified number of generations.

## Sample Output

Here's an example of what the output might look like:

```
Child (Generation 0): blood type AO
    Parent (Generation 1): blood type AB
        Grandparent (Generation 2): blood type AA
        Grandparent (Generation 2): blood type BO
    Parent (Generation 1): blood type OO
        Grandparent (Generation 2): blood type AO
        Grandparent (Generation 2): blood type OO
```

*Note:* The blood types are randomly assigned, so your output may vary each time you run the program.

## Customization

- **Adjusting Generations:**
  - Modify the `GENERATIONS` constant in `inheritance.c` to simulate more or fewer generations.
  - Example: Setting `const int GENERATIONS = 4;` will create a family tree with four generations.

- **Allele Representation:**
  - The program currently uses characters (`A`, `B`, `O`) to represent blood type alleles. This can be modified to include more complex genetic traits if desired.


## License

This project is licensed under the [MIT License](LICENSE).

