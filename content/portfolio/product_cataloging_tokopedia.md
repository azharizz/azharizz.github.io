---
title: Product Cataloging Tokopedia
type: page
---

{{< resize src="/images/product_cataloging.gif" width="480" height="480" alt="GIF_Page" >}}

# Problem

This project is a replication of a real Tokopedia project presented at the **START Summit Extension on February 24, 2022**, titled **"How We Leverage AI to Match Products."** It aims to improve the customer buying experience, which can sometimes be challenging—for example, searching for "KF 95 Masker" may return results where only 8 out of 10 products are actually related to KF 95, while the rest are KF94.

# Result

Before starting the product cataloging process, we cleaned and transformed the data with the following steps:

- Dropped missing values
- Normalized and transformed features
- Combined relevant features into one

Initially, most products were grouped into a single-member catalog, which had a Silhouette Score of 0.1828671.

To improve clustering quality, we applied **two** re-clustering methods:

**Member-to-Member re-clustering
→ Silhouette Score: 0.10205004**

**Member-to-Centroid re-clustering
→ Silhouette Score: 0.12488353**

## Repository
- [**Github Code**](https://github.com/azharizz/ecommerce_product_cataloging)
- [**RShiny Web Dashboard**](https://azharizz.shinyapps.io/ecommerce_shiny_azhar/)

