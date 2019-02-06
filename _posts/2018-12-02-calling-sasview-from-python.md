---
layout: post
title: Doing wedge integrations
subtitle: Calling SasView from python to do Wedge/Sector Integrations
gh-repo: /SasView/sasview
gh-badge: [star, watch, fork, follow]
tags: [develop, python, manipulations]
---

The code below exemplify how to call SasView as a library and call one of the many 
functions from the [manipulations](https://github.com/SasView/sasview/blob/master/src/sas/sascalc/dataloader/manipulations.py)
module.

Include your headers:

```python

from __future__ import print_function

import sys
import os

import numpy as np
from matplotlib import pyplot as plt

```

Find where your python library is.

RedHat usually stores it in this folder:
-   `/usr/lib/python2.7/site-packages/sasview-4.1-py2.7-linux-x86_64.egg`

Compiled from source for Ubuntu:
-   `/home/<your user name>/git/sasview/build/lib.linux-x86_64-2.7`

Compiled from source for MacOS:
-   `/Users/<your user name>/git/sasview/build/lib.macosx-10.11-x86_64-2.7`

```python

sasview_directory = '/Users/rhf/git/sasview/build/lib.macosx-10.11-x86_64-2.7'
sys.path.append(sasview_directory)

```

Let's import some SasView Classes:

```python
from sas.sascalc.dataloader.readers.red2d_reader import Reader
from sas.sascalc.dataloader.manipulations import Sectorcut, SectorQ
```

Initial parameters

```python
filename =  "my_file_Iqxy.dat" # Reduced QxQy file
phi_center =  0  # Phi Center in degrees
phi_width = 30  # Phi Width in degrees

```

Plot the sector integration in 2D

```python
def plot_iqxqy(data):
    '''
    @param data :: Output of Sasview Reader
    '''
    qx = data.qx_data
    qy = data.qy_data
    iqxqy = data.data
    # Reshape the data as 2D
    plt.figure()
    plt.scatter(qx, qy, c=np.log(iqxqy), s=50, edgecolor='', marker='s')
    plt.colorbar()
    # plt.show()
```

Plot the sector integration in 1D

```python
def plot_iq(data):
    '''
    @param data :: is 1D
    '''
    # Plot in 1D log scale
    plt.figure()
    plt.yscale('log', nonposy='clip')
    plt.xscale('log', nonposx='clip')
    plt.errorbar(data.x, data.y, yerr=data.dy)

```

Main SasView code to integrate the sector/wedge:


```python
def integrate_wedge(data, phi_center, phi_width, nbins=100):
    '''
    @param base: must be a valid base for an algorithm, i.e., a positive number
    The code for integration is here:
    https://github.com/SasView/sasview/blob/master/src/sas/sascalc/dataloader/manipulations.py
    '''
    phi_min = phi_center - phi_width/2.0
    phi_max = phi_center + phi_width/2.0

    print("Integrating from {} to {}".format(phi_min, phi_max))

    phi_min = np.deg2rad(phi_min)
    phi_max = np.deg2rad(phi_max)
    
    sector_wedge = SectorQ(r_min=0.0001, r_max=1, phi_min=phi_min, 
                           phi_max=phi_max, nbins=nbins)
    iq_wedge = sector_wedge(data)
    return iq_wedge
```

The code calling the functions above:

```python
r = Reader()
data = r.read(filename)
plot_iqxqy(data)
iq_wedge = integrate_wedge(data, phi_center, phi_width, nbins=50)
plot_iq(iq_wedge)
plt.show()

```