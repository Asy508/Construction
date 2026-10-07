# Proportional Integral Derivative (PID)
Its feedback mechanism automatic adjust a system at desired target.


## Why we need PID (The On/Off Problem)

Think of a standard home air conditioner. It uses On/Off control:
1. You set it to 24°C.
2. If the room hits 25°C, the compressor turns 100% ON.
3. Once the room drops to 23°C, the compressor turns COMPLETELY OFF.

This causes the temperature to constantly swing up and down like a wave. In a semiconductor cleanroom, a temperature or pressure swing of even 0.5°C can ruin millions of dollars worth of microchips. A PID loop fixes this by calculating exactly how much to open or close a valve (e.g., 42% open) to keep the line perfectly flat.

## How PID Works (Broken Down Simply)

A PID controller constantly calculates an Error (Error = Target Setpoint minus Current Actual Value) and uses three distinct mathematical steps to fix it:

1. Proportional (P) – "The Present Error"
  - How it works: The correction is directly proportional to the current error. If the error is large, the controller pushes hard. If the error is small, it pushes gently.
  - The Problem on its own: P-control can never actually reach the exact target. It will always fall slightly short (this is called steady-state error or offset) because as the error approaches zero, the pushing force drops to zero.
2. Integral (I) – "The Past Accumulated Error"
- How it works: The controller looks at the history of the error. If the system has been sitting slightly below the target for a long time, the Integral term sums up that history over time and adds extra force to eliminate the steady-state error, pushing the system right onto the target line.
- The Problem on its own: If it accumulates too much past error, it causes the system to overshoot the target.
3. Derivative (D) – "The Future Trend"
  - How it works: The controller looks at how fast the actual value is moving toward the target. It acts as a brake. If the value is rushing toward the target way too fast, the Derivative term applies a counter-force to slow it down, preventing it from overshooting.
