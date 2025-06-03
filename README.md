# Breaker Block Detection

## Changes
I noticed whilst recording the video that this line:
```
for j in range(displacement_timer):
```
was prone to occasionally looking ahead when looking for breakthrough candles as swing lows are not confirmed until at least `swing_length` candles afterwards so I changed it to
```
for j in range(swing_length, swing_length + displacement_timer):
```
It doesn't seem to affect the outcome too much
