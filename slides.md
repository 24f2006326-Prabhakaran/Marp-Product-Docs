---
marp: true
theme: my-product-theme
style: |
  /* Custom styling using Marp directives for code blocks */
  .center-code code {
    margin: 0 auto;
    width: 60%;
    text-align: left;
    display: block;
    background: #e9ecef;
    border: 1px solid #ced4da;
  }
paginate: true
header: 24f2006326@ds.study.iitm.ac.in
---

# 🚀 Product Documentation Overview
## Q3 Release: Core API v2.1

A technical overview for engineering stakeholders.

---

# Core Features: Data Ingestion

* **Efficiency:** Streamlined the data pipeline from 5 stages to 3.
* **Reliability:** Added dynamic fault tolerance and retry mechanisms.
* **Latency:** Reduced average ingestion time by **35%**.

<br>

## Algorithmic Complexity

We moved from a recursive search to an iterative hashing approach.

The time complexity is now $O(1)$ on average for lookup operations.

---

_class: inverse

# Algorithm Efficiency

The previous nested loop structure for index generation resulted in quadratic complexity:

$$
T_{old}(n) = O(n^2)
$$

The new hash-map-based process achieves near-constant time complexity:

$$
T_{new}(n) = O(1) + O(n) \cdot P_{\text{collision}}
$$

Where $P_{\text{collision}}$ is the probability of a hash collision.

---

![bg blur:1px](background.jpg)

# Scalability Roadmap

* Targeting 10,000 requests per second (RPS).
* Horizontal scaling planned for Q4.
* Cloud deployment finalized.

---

# Initialization Sequence

To start the ingestion service, use the following sequence:

<div class="center-code">
```bash
# Custom styling applied to this code block via the .center-code class
export API_KEY=abc-123
./ingestion-service --port 8080 --mode production
