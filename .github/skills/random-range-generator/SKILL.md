---
name: random-range-generator
description: 'Generate random numbers within a user-provided range. Use for random integer selection, sampling, and quick scripts that need min/max bounds validation.'
argument-hint: 'Provide min and max, optionally count and uniqueness requirement'
---

# Random Range Generator

Generate one or more random integers in an inclusive range `[min, max]`.

## When to Use
- You need a random integer between two bounds.
- You need multiple random values from a range.
- You want reproducible output by optionally seeding your generator.

## Inputs
- `min`: lower bound (integer)
- `max`: upper bound (integer)
- `count` (optional): how many numbers to generate (default: `1`)
- `unique` (optional): whether values must be unique (default: `false`)

## Procedure
1. Parse user input and normalize to integers.
2. Validate bounds and generation mode.
3. Choose command(s) based on shell and platform.
4. Run the command and return results.
5. Verify results satisfy the requested constraints.

## Decision Points
1. Bounds order:
- If `min > max`, swap values and note that normalization happened.

2. Uniqueness feasibility:
- If `unique = true`, require `count <= (max - min + 1)`.
- If infeasible, return an error and ask for adjusted inputs.

3. Output size:
- If `count = 1`, return a single value.
- If `count > 1`, return one value per line for easy reuse.

## Commands

### zsh/bash (single value)
```bash
min=<min>; max=<max>; echo $((RANDOM % (max - min + 1) + min))
```

### zsh/bash (multiple values, allow duplicates)
```bash
min=<min>; max=<max>; count=<count>
for ((i=0; i<count; i++)); do
  echo $((RANDOM % (max - min + 1) + min))
done
```

### zsh/bash (multiple unique values)
```bash
min=<min>; max=<max>; count=<count>
jot "$((max - min + 1))" "$min" "$max" | sort -R | head -n "$count"
```

### PowerShell (single value)
```powershell
Get-Random -Minimum <min> -Maximum (<max> + 1)
```

### PowerShell (multiple values)
```powershell
1..<count> | ForEach-Object { Get-Random -Minimum <min> -Maximum (<max> + 1) }
```

## Completion Checks
- Every generated number `n` satisfies `min <= n <= max`.
- Output count equals requested `count`.
- If `unique = true`, no duplicates are present.
- Any normalization (such as swapped bounds) is explicitly reported.

## Example Prompts
- `Generate a random number between 10 and 25.`
- `Generate 5 random numbers between -3 and 3.`
- `Generate 8 unique random numbers between 1 and 20.`
