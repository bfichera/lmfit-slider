# lmfit-slider

### Requirements
- `matplotlib`
- `numpy`

### Usage

```
import lmfit
import matplotlib.pyplot as plt
import numpy as np

from slider import slider


def fcn(params, x):
    return np.sin(params['k']*x)


params = lmfit.Parameters()
params.add('k', value=0, min=-10, max=10)

x = np.linspace(0, 2*np.pi, 100)


slider(fcn, params, x=x, args=(x,))
```
