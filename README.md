# lmfit-slider

### Requirements
- `matplotlib`
- `numpy`

### Usage

```
import lmfit
import matplotlib.pyplot as plt
import numpy as np

from lmfit_slider import slider


def fcn(params, x):
    return np.sin(params['k']*x)


params = lmfit.Parameters()
params.add('k', value=1, min=-10, max=10)

x = np.linspace(0, 2*np.pi, 100)
y = np.sin(4*x)


new_params = slider(fcn, params, x=x, data=y, args=(x,))

new_params.pretty_print()
```
