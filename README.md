# Genetic inheritance simulator

A C exercise that constructs a three-generation family tree and randomly passes one blood-type allele from each parent to each child.

```text
grandparents (random A / B / O)
          ↓ one allele from each parent
       parents
          ↓
         child
```

## Run

```sh
cc -Wall -Wextra -Werror inheritance_inheritance.c -o inheritance
./inheritance
```

Each run seeds the random generator with the current time, so the output varies. [`inheritance_inheritance.c`](inheritance_inheritance.c) contains family creation, printing and recursive cleanup.

**Model limit:** This is a simplified educational simulation of allele inheritance, not a clinical blood-typing tool. [License](LICENSE).
