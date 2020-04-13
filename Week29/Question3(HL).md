# Corona vs Gold Price #
```
import numpy as np
import matplotlib.pyplot as plt

gold = np.array([1584, 1595, 1593, 1625, 1638, 1674, 1674, 1700, 1675, 1661, 1646, 1641, 1594, 1511, 1581,1555, 1468, 1493, 1481, 1469, 1483, 1495, 1490, 1516, 1622, 1610, 1627, 1624, 1625, 1626, 1613])

corona = np.array([88585, 90443, 93016, 95314, 98425, 102050, 106099, 109991, 114381, 118948, 126214, 134509, 145416, 156475, 169511, 182431, 198161, 218843, 244988, 275680, 305132, 337612, 179105, 422940, 471497, 532491, 597044, 663805, 724220, 786006, 859798])

plt.xlim(1465, 1700)
plt.ylim(88000, 960000)
plt.title("Gold price vs Corona cases", fontsize=20)
plt.xlabel("Gold price (USD)")
plt.ylabel("Corona cases (people)")

plt.scatter(gold, corona, s=50, c ="b", marker="D", alpha=0.5)
plt.show()
```
##
