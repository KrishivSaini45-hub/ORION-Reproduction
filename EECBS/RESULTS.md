# EECBS Reproduction Results

## Environment

- OS: Ubuntu 22.04
- Compiler: GCC 11.4.0
- Build: CMake (Release)

---

## Benchmark Configuration

| Parameter | Value |
|-----------|-------|
| Map | random-32-32-20.map |
| Scenario | random-32-32-20-random-1.scen |
| Number of Agents | 50 |
| Runtime Limit | 60 seconds |
| Suboptimality | 1.2 |

---

## Execution Command

```bash
./eecbs \
-m random-32-32-20.map \
-a random-32-32-20-random-1.scen \
-o test.csv \
--outputPaths=paths.txt \
-k 50 \
-t 60 \
--suboptimality=1.2
```

---

## Output

```text
WDG+R+C+T+BP with AStar : Succeed,1174,0.078822,6,46842,1128,1082,1128,
```

---

## Observations

- Successfully compiled the EECBS implementation.
- Successfully executed the benchmark example provided by the authors.
- A valid solution was found for **50 agents**.
- Runtime was approximately **0.079 seconds**.
- Final solution cost: **1174**.
- The solver completed successfully while satisfying the specified suboptimality bound.
