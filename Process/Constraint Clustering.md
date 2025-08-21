# Goals:
1. Avoid overcounting.
2. Reduce the risk of *getting it right* but not reaping the rewards.
3. Simplify the setting.
### Avoid Overcounting
There exist sets of constraints that are mutually exclusive (or roughly mutually exclusive). If we were to model each constraint independently, then our predicted values would be too high in such settings.

For example, one constraint may dominate another, or two constraints may share a monitored element but have different contingencies. At any single point in time, at most one such constraint can bind (roughly; there exist exceptions, but this is an approximation with which we are comfortable).
### Reduce the risk of *getting it right* but not reaping the rewards
There exist settings in which, even when given that one of a handful of constraints will bind, it's difficult to predict which one.

For example, it is possible for us to correctly forecast congestion within a given corridor but choose a path that targets the wrong constraint within that corridor. This could lead to a situation in which our prediction is correct, but we realize a loss.

When we're able to predict something, we want to capitalize.
### Simplify the setting
There are seemingly innumerable constraints to model. We prioritize tractability by focusing on constraint clusters.

---
## Approach
**Unit Depth Property:** at any point in time, at most one constraint in cluster should have positive modeled shadow price.