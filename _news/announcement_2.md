---
layout: post
title: Highway to... Determining Fatal Outcomes in Traffic Accidents
headline: |
    Paper accepted at BRACIS 2025!
    
    Highway to... 
    Determining Fatal Outcomes in Traffic Accidents Based on Police Reports
date: 2025-06-23 16:11:00-0400
inline: false
related_posts: true
giscus_comments: true
image: /assets/img/bracis_logo_2025.png 
categories: news research conference publication
tags: [paper, bracis, conference, xAI, "road safety"]
---

<style>body {text-align: justify}</style>


<div style="float: right; margin: 0 0 1em 1em;">
  <img src="/assets/img/bracis_logo_2025.png" alt="Descrição da imagem" width="250">
</div>

The paper _Highway to… Determining Fatal Outcomes in Traffic Accidents Based on Police Reports_ just got accepted for publication at the [35th Brazilian Conference on Intelligent Systems (BRACIS)](https://bracis.sbc.org.br/2025/). The paper is authored by Arthur M. P. Gabardo[^1], Guilherme A. A. Schünemann, [Pablo A. Jaskowiak](https://pajaskowiak.github.io)[^1], Benjamin G. Moreira[^1], and Ricardo J. Pfitscher[^1].

The paper addresses Brazil’s ongoing road safety challenges, particularly the high number of fatal accidents on its federal highways. With one of the largest road networks in the world, the country faces significant social and economic impacts from traffic-related incidents. This study presents a case analysis focused on the southern region of Brazil, applying and comparing three machine learning models — Random Forest (RF), k-Nearest Neighbors (kNN), and Multilayer Perceptron (MLP) — to classify the severity of road accidents.

Using open data provided by the Brazilian Federal Highway Police (PRF) from 2021 to 2024, extensive preprocessing was conducted, including categorical variable encoding, feature selection, and the application of the SMOTE technique to mitigate class imbalance. The models were evaluated using key performance metrics such as specificity, F1-score, and AUC-ROC. Among the findings, both RF and kNN (with SMOTE) demonstrated excellent performance in predicting fatal accidents, each achieving an AUC-ROC of 0.99. In addition to model evaluation, the paper includes a post-hoc analysis using Shapley Additive Explanations (SHAP) to identify the most influential features associated with accident severity, providing valuable insights into the factors that contribute most to fatalities on Brazilian highways.

As detailed in the [conference website](https://bracis.sbc.org.br/2025/): “BRACIS is one of the most important events in Brazil for researchers aiming to publish significant and novel results in the fields of Artificial Intelligence (AI) and Computational Intelligence (CI). It was established through the merger of the two most prominent scientific events in Brazil dedicated to AI (SBIA) and CI (SBRN).”

As soon as the paper is out, it will be linked in the publications page.

[^1]: Researchers affiliated with the IDA Lab – UFSC.
