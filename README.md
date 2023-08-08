# Tracking error calculations:

## 

## Currency decomposition

The portfolio weights are $w_{i}$ for each assets $i$. The price of the asset in local currency is $P_{l, i, t}$ and the exchange rate of the local currency to the reference rate is $E_{r, l, t}$ for period $t$. The local currency refers to the currency of denomination of the asset, this is, for the Apple stock it would be USD and the exchange rate is, for a chilean based fund, would use $E_{r, l, t}$ which is the price on one USD in CLP. If we use logarithmic returns we have:

\equation{begin}
P_{r, i, t} = P_{l, i, t} * E_{r, l, t}
\equation{end}

Where $P_{r, i, t}$ corresponds to the price of the asset in the reference currency. 

\equation{begin}
ret_{r, i, t} = ln\left(\frac{P_{l, i, t}}{P_{l, i, t-1}}\frac{E_{r, l, t}}{E_{r, l, t-1}}\right)
\equation{end}
