# Why Income Alone Won't Solve Plastic Pollution — But It's Still Half the Story

*A short brief based on my analysis of 2020 plastic pollution and GDP data across 204 countries*

## The question I wanted to answer

Most conversations about plastic pollution rank countries by total waste — which mostly just tells you who has the most people, not who's managing pollution well or badly. I wanted to strip population out of the picture and ask a more useful question: **does a country's income level actually predict how much plastic pollution each person in that country produces?**

I ran the numbers myself using public data (Our World in Data's plastic pollution dataset, World Bank GDP figures, and population data), merged for 204 countries in 2020, and tested it with a regression model.

## What I found

Income matters — a lot. Once I calculated pollution on a per-person basis, the relationship with GDP per capita was strong and statistically clear: **higher-income countries generate significantly less plastic pollution per person**, and income alone explains about half (R² = 0.505) of the difference between countries. That's not a small effect for a single variable.

But half is also the important number here. Income explains a lot — it doesn't explain everything. The other half of the story is presumably things like waste infrastructure, regulation, urban planning, and how seriously a government treats waste management, none of which I measured directly here.

## Where Pakistan fits in

Pakistan's numbers actually land close to where the trend would predict for a country at its income level (GDP per capita ~$5,135). Its pollution per capita (0.0109) is almost identical to Bangladesh's, even though Bangladesh's income is noticeably higher. And compared to Nigeria — a country with income similar to Bangladesh but nearly 60% more pollution per capita — Pakistan is doing relatively better than its income level alone would suggest.

That's not something to celebrate uncritically. It just means Pakistan isn't an outlier in either direction; it's roughly where you'd expect a country at this income level to sit. The countries worth studying more closely are the outliers — like Nigeria, which pollutes far more than its income predicts, or wealthy countries that still pollute more than expected once you look past the income trend.

## What this means for policy, in plain terms

1. **Waiting for economic growth to fix plastic pollution isn't a strategy on its own.** Growth helps — the data backs that up clearly — but it's a slow lever, and it only accounts for half the variation. Countries can't just assume pollution will fall as GDP rises without also investing directly in waste collection and management.

2. **The interesting cases are the outliers, not the average.** Countries that pollute far more or far less than their income level predicts are the ones worth studying for lessons — what are lower-pollution outliers doing right at their income level that others aren't?

3. **For a country like Pakistan**, the data suggests we're not doing unusually badly for our income bracket — but "not unusually bad" is a low bar. The real opportunity is in the other half of the story: policy and infrastructure choices that could move Pakistan into outlier territory in the good direction, the way some countries manage to outperform their income level.

## A limitation worth being upfront about

This is one year of data, and it shows association, not proof of cause and effect. Income could reduce pollution through better infrastructure — or a third factor, like stronger regulation or more urbanization, could be driving both higher income and lower pollution independently. I'd want time-series data and more variables (regulation strength, urbanization rate, recycling infrastructure) before treating this as a causal claim rather than a strong pattern.
