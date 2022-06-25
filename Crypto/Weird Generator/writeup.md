# Weird generator

The prime generated in the challenge is in the form of 2 * g * r + 1 while g is known and r remain unknown. Both g and r is 512-bit integer.

So $n = (2gr + 1) (2gs + 1)$ implies $\phi(n) = 4g^2rs$. Since $g$ is known, all we need is to calculate for $rs$

$$n = 4g^2rs + 2gr + 2gs + 1$$
$$\implies \frac{n - 1 }{4g^2}= rs + \frac{r + s}{2g}$$

Since r, s and g are all 512-bit numbers the value of the later fraction range from -2 to 2. Then divide both sides by $4g^2$ will approximates the value of $rs$ with an error within 2 unit. Check for each case and get the flag.

Full script is [here](./solver.py)

**P/S**: The original problem is not that easy, and I don't even know the source of the problem. Sorry about that.