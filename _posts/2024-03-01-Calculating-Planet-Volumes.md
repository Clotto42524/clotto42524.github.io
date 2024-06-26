---
layout: post
title: Calculating Planet Volumes
image: "/posts/planets.jpg"
tags: [Python, Planets]
---

This is a small project demonstrating the use of NumPy to calculate the volumes of each of the planets in our Solar System... and more!

---

First we start by importing numpy

```python
import numpy as np
```

Next, after doing some googling, we create an array with the radii of each planet saved as **radii**.


```python
radii = np.array([2439.7, 6051.8, 6371, 3389.7, 69911, 58232, 25362, 24622])
```

We know that there is a specific formula for calculating the volume of a sphere. We'll set that equal to **volume**

```python
volume = 4 / 3 * np.pi * r ** 3
```

Now we'll substitute in our array and set that equal to **volumes** (since it's multiple volumes) and print

```python
volumes = 4 / 3 * np.pi * radii ** 3
print(volumes)
>>> 
[6.08272087e+10 9.28415346e+11 1.08320692e+12 1.63144486e+11
 1.43128181e+15 8.27129915e+14 6.83343557e+13 6.25257040e+13]
```

We can also do this for an array of any number... one million, for instance.

```python
radii = np.random.randint(1, 1000, 1000000)
volumes = 4 / 3 * np.pi * radii ** 3
print(volumes)
>>> 
[2.06523693e+06 7.75734624e+05 1.08269693e+09 ... 3.05362806e+03
 3.40154939e+07 8.24479576e+07]
```

