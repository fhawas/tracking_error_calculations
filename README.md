# Tracking error calculations:

## 

## Currency decomposition

The portfolio weights are $w_{i}$ for each assets $i$. The price of the asset in local currency is $P_{l, i, t}$ and the exchange rate of the local currency to the reference rate is $E_{r, l, t}$ for period $t$. The local currency refers to the currency of denomination of the asset, this is, for the Apple stock it would be USD and the exchange rate is, for a chilean based fund, would use $E_{r, l, t}$ which is the price on one USD in CLP. If we use logarithmic returns we have:

$$ P_{r, i, t} = P_{l, i, t} * E_{r, l, t} $$

Where $P_{r, i, t}$ corresponds to the price of the asset in the reference currency. 

$$ ret_{r, i, t} = ln\left(\frac{P_{l, i, t}}{P_{l, i, t-1}}\frac{E_{r, l, t}}{E_{r, l, t-1}}\right) $$

which means,

$$ ret_{r, i, t} = lret_{l, i, t} + lrete_{l, r, t} $$

where the logarithmic return of the asset in local currency is,

$$ lret_{l, t, t} =  ln\left(\frac{P_{l, i, t}}{P_{l, i, t-1}}\right) $$

and the logarithmic return of the exchange rate is,

$$ lrete_{l, t, t} =  ln\left(\frac{E_{r, l, t}}{E_{r, l, t-1}}\right) $$

The tracking error for the portfolio is,

$$\sum_{i}\sum_{j} w_{i} w_{j} cov\left(ret_{r, i, t}, ret_{r, j, t}\right) $$

is equal to,

$$\sum_{i}\sum_{j} w_{i} w_{j} \left( cov\left(lret_{l\left(i\right), i, t}, lret_{l\left(j\right), j, t} \right) + cov\left(lret_{l\left(i\right), i, t}, lrete_{l\left(j\right), r, t} \right) + cov\left(lrete_{l\left(i\right), r, t}, lret_{l\left(j\right), j, t} \right) + cov\left(lrete_{l\left(i\right), r, t}, lrete_{l\left(j\right), r, t}\right) \right)$$

The above corresponds to a extended portfolio composed of assets in local currencies and the currency portfolio. The correlation matrix will contain both returns in local currency and the currency returns expressed in the reference currency.
