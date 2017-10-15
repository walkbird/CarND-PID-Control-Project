# CarND-Controls-PID
Self-Driving Car Engineer Nanodegree Program

## Reflection

### Effect of P component

P component will help the car go back to the target position. If tau_p is too small, the car will leaves the road when entering a turn (See video "p_small.m4v", tau_p = 0.003 ); And if tau_p is too large, the car will change direction rapidly, and oscillations fast  (See video "p_large.m4v", tau_p = 5 ). My final choice of tau_p is 0.3;

### Effect of D component

D component will help the car converging to the target position. If tau_d is too large, the car will oscillations fast around the target position (See video "d_large.m4v", tau_d = 100); And if tau_d is too small, the car will not be able to converge to the target position, and oscillations with a large range (See video "d_small.m4v", tau_d = 0.01). My final choice of tau_d is 5;

### Effect of I component

I component is used to fix systematic bias. If tau_i is too large, the CTE will accumulate too fast, resulting in a big steering value and leaving far away from the target position (See video "i_large.m4v", tau_i = 0.1). If tau_i is too small, it will take too long to compensate systematic bias. My final choice of tau_i is 0.00002;

## Final choice of combination

* tau_p = 0.3
* tau_d = 5
* tau_i = 0.00002