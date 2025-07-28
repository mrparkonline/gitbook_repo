# Mean, Median, Mode

{% hint style="success" %}
Mean, median and mode are ways to summarize a numerical dataset by calculating to a singular number.
{% endhint %}

## Mean

The average of all numbers in the dataset.

<figure><img src="../../.gitbook/assets/summation.webp" alt="" width="188"><figcaption><p>The summation symbol</p></figcaption></figure>

```
The mean formula:

mean is equal to the sum of all data points divided by 
the total number of data points.
```

$$
mean = \frac{\sum_{}{} x_i}{n}
$$

x<sub>i</sub> is each data point at index `i`

`n` represents the total number of data points

### Example

| Poker earnings from 12 table games. |
| ----------------------------------- |
| $12                                 |
| $37                                 |
| $5                                  |
| $28                                 |
| $44                                 |
| $19                                 |
| $7                                  |
| $50                                 |
| $22                                 |
| $11                                 |
| $33                                 |
| $41                                 |

The following table above is the monetary earnings made from 12 poker games. We will be calculating the mean of this dataset.

#### Sum of all earnings (each data points all added up)

$$
sum = 12 + 37 + 5 + 28 + 44  + 19 + 7 + 50 + 22 + 11 + 33 + 41 = 309
$$

#### Total Number of data points: 12

$$
mean = \frac{309}{12} = 25.75
$$

> **Conclusion**
>
> The calculated mean equals `25.75`.
>
> The player made `$309` in `12` table games, and on average the player made `$25.75`

## Median

The middle-most data point in a dataset.

{% hint style="danger" %}
When calculating the median, the dataset must be sorted.
{% endhint %}

Steps to calculate the median:

1. Sort the dataset from least to greatest
2. If the data set has odd number of data points, the middle value is the **median**
3. If the data set has even number of data points, then calculate the mean of the two middle most values.

### Example with odd number of data points

$$
data = \{3, 1, 4, 1, 5\}
$$

The following above contains 5 data points.

When sorted we get: `{1, 1, 3, 4, 5}`

The middle-most data point after the sorting is the value: `3.`

Therefore, **the median of the value is 3.**

### Example with even number of data points

$$
poker = \{12,37,5,28,44 ,19,7,50,22,11,33,41\}
$$

The following set above contains our previous 12 data points with our poker earnings. When sorted, we get following order:

$$
poker = \{5, 7, 11, 12, 19, 22, 28, 33, 37, 41, 44, 50\}
$$

In this dataset, there are even number of data points; therefore, we must calculate the mean of the two middle data points.

* 6th number: **22**
* 7th number: **28**

$$
median = \frac{22+28}{2} = 25
$$

> **Conclusion**
>
> In the data set of poker earnings, there are 6 data points total where the dollars earned was lower than the median of $25.
>
> Since the data set has 12 data points, the remain 6 earnings were above the median.

## Mode

The most occuring data point in a dataset.

{% hint style="danger" %}
A data set can have the following properties:

* **Unimodal** (one mode)
* **Bimodal** (two modes)
* **Multimodal** (more than two)
* Or **have no mode** at all.
{% endhint %}

### Unimodal: Just one mode

$$
data = \{1, 2, 2, 3, 4\}
$$

The dataset above has a mode of `2`.

_2 was the most occurring data point, and it is unimodal no other data points were repeated._

### Bimodal: two modes

$$
data = \{3, 4, 4, 5, 6, 7, 7, 8\}
$$

The dataset above has a mode of `4` and `7`.

_3 and 7 both occurred twice in the dataset. Hence, this dataset is bimodal._

### Multimodal: more than two

$$
data = \{2, 2, 3, 3, 4, 4, 5, 6\}
$$

The dataset above has a mode of `2, 3, 4`.

_Values of 2, 3 and 4 occur twice in the dataset making the dataset multimodal._

### No mode

$$
data = \{1, 2, 3, 4, 5\}
$$

The dataset has no repeating values; therefore, there is no mode.
