# Example: From derivative rules to partial derivatives

This example demonstrates the learning workflow rather than prescribing exact wording.

## Learner request

> I do not understand partial derivatives.

## Diagnose the dependency

Before explaining partial derivatives, check whether the learner can use the ordinary power rule:

```text
Find d/dx of x^4.
```

If the learner answers `3x^3`, the exact gap is that the new coefficient must be the original exponent.

## Repair

Explain only the missing rule:

```text
d/dx(x^n) = n x^(n-1)

d/dx(x^4) = 4x^3
```

Use a second example with a coefficient:

```text
d/dx(2x^3) = 6x^2
```

## Reproduction test

Ask the learner, without showing the answer:

```text
Find d/dx of 3x^2 + 2x + 4.
```

A correct answer, `6x + 2`, demonstrates reproduction of the basic derivative rules.

## Connect to the new concept

Introduce:

```text
f(x, y) = 3x^2 + 2y
```

Explain that `f_x` differentiates with respect to `x` while treating `y` as a constant, and `f_y` does the reverse:

```text
f_x = 6x
f_y = 2
```

## Transfer test

Change the structure by adding a mixed term:

```text
f(x, y) = x^2 + 3xy + y^2
```

Ask for both partial derivatives. A successful learner should obtain:

```text
f_x = 2x + 3y
f_y = 3x + 2y
```

This provides stronger evidence than simply recognising the worked answer.

