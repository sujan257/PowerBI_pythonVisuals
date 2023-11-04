# The following code to create a dataframe and remove duplicated rows is always executed and acts as a preamble for your script: 
# dataset = pandas.DataFrame(energy_%)
# dataset = dataset.drop_duplicates()

# Paste or type your script code here:
import matplotlib.pyplot as plt
import numpy as np

import matplotlib.pyplot as plt
import pandas as pd
import numpy as np

plt.figure(facecolor='#212121')

# plot polar axis
ax = plt.subplot(111, polar=True)

# remove grid
plt.axis('off')

# Set the coordinates limits
upperLimit = 100
lowerLimit = 10

# Compute max and min in the dataset
max = 100

# Let's compute heights: they are a conversion of each item value in those new coordinates
# In our example, 0 in the dataset will be converted to the lowerLimit (10)
# The maximum will be converted to the upperLimit (100)
slope = (max - lowerLimit) / max
heights = 5

# Compute the width of each bar. In total we have 2*Pi = 360°
width = 2*np.pi / 100

# Compute the angle each bar is centered on:
indexes = list(range(1, 101))
n = int(dataset['energy_%'])
angles = [element * width for element in indexes[:n]]
angles1 = [element * width for element in indexes[n:]]

# Draw bars
label = str(n)+"%"
ax.text(0.5 , 0.5, label,
        horizontalalignment='center',
        verticalalignment='center',
        fontsize=50,
        color='#1DB954',
        transform=ax.transAxes)
ax.text(0.5 , 0.35, "Energy",
        horizontalalignment='center',
        verticalalignment='center',
        fontsize=30,
        color='#808080',
        transform=ax.transAxes)
ax.set_facecolor("#636262")
bars = ax.bar(
    x=angles, 
    height=heights, 
    width=width, 
    bottom=lowerLimit,
    linewidth=2,
    color='#1DB954', 
    edgecolor="#212121")
bars2 = ax.bar(
    x=angles1, 
    height=heights, 
    width=width, 
    bottom=lowerLimit,
    linewidth=3, 
    color='#808080',
    edgecolor="#212121")
plt.show()
