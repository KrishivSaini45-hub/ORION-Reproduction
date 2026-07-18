# MAPF-LNS2 Reproduction Results

## Environment

- OS: Ubuntu 22.04
- Compiler: GCC 11.4.0
- CMake: Release Build
- Libraries:
  - Boost
  - Eigen

---

## Benchmark Configuration

| Parameter | Value |
|-----------|-------|
| Map | random-32-32-20.map |
| Scenario | random-32-32-20-random-1.scen |
| Number of Agents | 400 |
| Runtime Limit | 300 seconds |

---

## Execution Command

```bash
./lns \
-m random-32-32-20.map \
-a random-32-32-20-random-1.scen \
-o test \
-k 400 \
-t 300 \
--outputPaths=paths.txt
```

---

## Output

```text
InitLNS(PP): runtime = 13.3903, iterations = 712, colliding pairs = 0,
initial colliding pairs = 460, solution cost = 21374,
initial solution cost = 17746, failed iterations = 449

LNS(PP;PP): runtime = 13.393, iterations = 1,
solution cost = 21374, initial solution cost = 21374,
failed iterations = 1
```

---

## Observations

- Successfully built the MAPF-LNS2 implementation using CMake.
- Successfully executed the authors' benchmark example.
- The initial solution contained **460 colliding agent pairs**.
- Large Neighborhood Search resolved all collisions.
- A collision-free solution was generated for **400 agents**.
- Final solution cost: **21,374**.
- Total runtime: **13.39 seconds**.
