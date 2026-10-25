# Animation Graph

[Leia em português](README.md)

## State machine setup

To play animations, create a **State Machine** and connect its output (`Output`).

![State machine connected to the output](images/state-machine-output.png)

Add states for the animations and a transition state. **Only one transition state is supported.** Set one animation state as the default and leave it unconnected to parameters; it will be the default fallback state.

![Animation and transition states](images/states-and-transition.png)

## Control parameters

Use custom parameters to control animation flow. Set these parameters from code.

![Custom parameters](images/custom-parameters.png)

The assignment API uses the `Set` prefix followed by the corresponding data type.

![Parameter assignment methods](images/parameter-set-methods.png)

The method/function's first argument must match the parameter name in the Animation Graph. Its second argument must match that parameter's data type.

### Flag vs. Trigger

![Flag and Trigger parameters in the Animation Graph](images/trigger-parameter.png)

`Flag` represents a boolean state (`true`/`false`) that remains set until changed. `Trigger` is a one-shot signal: it activates the associated transition or action once, rather than keeping a boolean state active.

## Recommendation

Avoid using raw strings to identify parameters. Consider using an `enum` and a `switch` to return the correct parameter name, or constants (`const`) for a simpler approach. This reduces typos and makes the code easier to maintain.
