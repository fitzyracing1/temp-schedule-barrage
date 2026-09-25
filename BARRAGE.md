# Temp Schedule

> The AI does one invent pass at high heat, then two low-heat passes — first it builds, then it freezes and checks the money metric.

## Purpose
Run every job in three named passes. The names are high, low, low. Heat stays the same on both lows. The last low only changes what the work is allowed to do.

## How it works (plain English)
1. Start hot. Invent the idea. Do not ship it.
2. Cool to low. Build the real file or plan.
3. Stay at the same low. Freeze the result and make the metric `2 times x times c minus d equals 1` hold.
4. Stop. Do not go back to high.

## Key ideas
- High (hot inventing)
- Low first (building)
- Low second (locking and checking the metric)
- T (just means temperature)

## The actual code
```
Temp_schedule = ["high", "low", "low"]
# high   → invent
# low    → build
# low    → freeze + enforce metric
```

## Line-by-line translation
1. Temp_schedule = ["high", "low", "low"] → “three passes in this exact order”
2. high → invent → “first pass only dreams up the work”
3. low → build → “second pass makes the thing”
4. low → freeze + enforce metric → “third pass locks it and checks 2xc − d = 1”

## Decisions the program makes
- If pass is 1 → invent at high
- If pass is 2 → build at low
- If pass is 3 → freeze and enforce the metric at the same low
- If someone asks to return to high after pass 1 → refuse

## Commercial note
Potential: High  
Estimated value: control layer for every other runner  
Recommendation: Keep developing

## Current status
Finished shape for human reading. Skill file lives in its own repo.

## Next step for human reader
Point a job name and a lane at the runner and let the three passes run.
