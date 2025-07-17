---
layout: post
title: Isolation Forest for Robust Anomaly Detection
headline: |
    Paper accepted at CBIC 2025!
    
    An Isolation Forest Approach for Robust Anomaly Detection in 
    Industrial Machines Using Out-of-Distribution Acoustic Data
    
date: 2025-07-16 23:11:00-0400
inline: false
related_posts: true
giscus_comments: true
image: /assets/img/publication_preview/cbic_2025_padded_a4.png
categories: news research conference publication
tags: [paper, cbic, conference, isolation forest, anomaly detection, out of out-of-distribution]
---

<style>body {text-align: justify}</style>


<div style="float: right; margin: 4em 0 1em 1em;">
  <img src="/assets/img/publication_preview/cbic_2025.png" alt="Descrição da imagem" width="250">
</div>

Our paper on anomaly detection in industrial machines was accepted for presentation at [**CBIC 2025**](https://cbic2025.dcc.ufmg.br/). The paper is titled _An Isolation Forest Approach for Robust Anomaly Detection in Industrial Machines Using Out-of-Distribution Acoustic Data_. The paper is a collaboration by Cristofer Silva[^2], João Campos[^3], Leonardo Afonso Ferreira Bortoni[^1], [Pablo Andretta Jaskowiak](https://pajaskowiak.github.io)[^1], Diego Pinheiro[^3]. It investigates whether simpler, more interpretable methods can match the performance of deep learning approaches in the task of detecting acoustic anomalies in mechanical equipment. While recent literature has focused heavily on neural networks, we explore a baseline combining:

- **MFCCs (Mel-Frequency Cepstral Coefficients)** for audio feature extraction  
- **Isolation Forest**, a classical tree-based anomaly detection algorithm

The experiments were conducted on the **MIMII dataset**, which includes real recordings of operating and faulty industrial components such as pumps, fans, and valves. Results indicate that this lightweight pipeline performs comparably to more complex models, particularly in **out-of-distribution** conditions—when the test data differs significantly from the training set. This suggests that interpretable models may remain a viable option in practical, resource-constrained industrial scenarios.

From the [CBIC 2025 website](https://cbic2025.dcc.ufmg.br/) (translated): "_The Brazilian Congress on Computational Intelligence (CBIC) is a biennial event that was initially organized as the Brazilian Congress on Neural Networks, as it was promoted by the Brazilian Society of Neural Networks, later succeeded by the Brazilian Society of Computational Intelligence (SBIC). The first edition took place in Itajubá in 1994, and the most recent one (16th edition) was held in 2023, in Salvador, Bahia._"

The full paper will be presented at the conference and will be available soon.

[^1]: Researchers affiliated with the IDA Lab – UFSC.
[^2]: Universidade de Pernambuco (UPE), Recife, Brazil.
[^3]: Universidade Católica de Pernambuco (UNICAP), Recife, Brazil.
