---
title: "SACA - Impact"
layout: textlay
excerpt: "Our Impact on Industry"
sitemap: false
permalink: /impact/
---

# Impact on Industry and Academia

In this page, we highlight the main inventions of SACA members that have had direct impact on industry. Beyond the several tools and ideas we contributed to various defense agencies, we hightlight the public ones that have impacted public features in industrial products:

#### Cryptographic Shredding/Erasure for Secure Non-Volatile Memory
Back in 2015, we have invented and pioneered the first work that addresses secure data erasure in emerging non-volatile memory. The paper was published in ASPLOS'16 [Silent Shredder](https://dl.acm.org/doi/10.1145/2980024.2872377), where we discussed how using different encryption keys, manipulating nonces, etc., can be used to effectively and securely erase data. These insights and very similar techniques are used today in Intel's Optane Persistent Memory as the [Secure Erase](https://software.intel.com/content/www/us/en/develop/articles/how-to-securely-erase-data-on-intel-optane-persistent-memory.html) feature.


#### Crash Consistency for Secure NVMs
The crash consistency issue caused by losing the contents of security metadata cache was first discovered and discussed in our ASPLOS'16 [Silent Shredder](https://dl.acm.org/doi/10.1145/2980024.2872377) paper in Section 7.1. This issue has been later picked up by academia and led to hundreds of papers in this domain that are addressing this problem.

#### Identifying the Issue of High Recovery Time for Secure NVMs
Our papers (Triad-NVM and Anubis) are the first to discuss the high recovery time in secure crash consistent memories. Rebuilding integrity tree requires iterating over data blocks and hence takes hours. More recent studies show that just sanitizing a 512GB DCPMM DIMM can take an hour (https://dl.dell.com/topicspdf/dcpmm-user-guide_en-us.pdf). Our work is also the first to show how to speed up recovery time to be less than a second, for a negligible performance overhead.

#### Identifying and Solving Recovery Challenges for Tree-of-Counters (ToCs) in Secure NVMs
We are the first group to identify the challenges for recovering SGX-like ToC integrity trees in integrity-protected NVMs. Our papers (Anubis and Phoenix) are also the first to propose low-overhead recovery schemes for such parallelizable integrity trees. 

#### Next?
We are confident that several of our contributions and ideas will be deployed in industry 5-10 years down the road, once future technologies become widely used. Today, we think of the issues and features the industry can leverage 5-10 years later.
