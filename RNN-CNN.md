# RNN /CNN

The following text is a summary based on Géron (2019) pp. 497-524.

RNNs suffer from two main problems:
+ unstable gradients
+ short terms memory

For specific use cases, other architectures like Dense Networks or CNN can be useful.

### Formal description
A RNN could be described as a reflexive system:
**x** describes a function's -**f()**- input vector while **y** describes the functions output. RNN are reflexive as they consume their previous output(s) (**x**<sub>t-1</sub>). Hence, output **y**<sub>t</sub> with with t = 2 would be a function of f(**x**<sub>t</sub> + **y**<sub>t-1</sub> + b) where **y**<sub>t-1</sub> = f(**x**<sub>t-1</sub>).

Including weights (K as activation function):

**y**<sub>t</sub> = K(**W**<sub>x</sub><sup>T </sup>**x**<sub>t</sub> +
  **W**<sub>y</sub>**y**<sub>t-1</sub>+ **b**)

This reflexivity as also called memory.
