# Recommender Systems for Tailored Testing: An R Tutorial

This repository provides a tutorial on how to use recommender systems — specifically collaborative filtering with matrix factorization (Funk SVD) — to improve the relevance of test items in a longitudinal assessment setting.  

The example uses **hypothetical data** to illustrate how these techniques can be applied in educational measurement and psychometrics.  

---

## Motivation

In many longitudinal or formative assessment programs, participants are asked to provide **feedback** (e.g., rating the relevance of questions). These ratings can be used to build a recommender system that predicts which future questions are most likely to feel relevant for new participants.  

This tutorial walks through:
1. Simulating item relevance ratings data
2. Using the `recommenderlab` package in R to fit a recommender system with Funk SVD
3. Generating predicted ratings for "unseen" items
4. Discussing how predictions could inform tailored item selection in a hypothetical assessment context

---

## Key Idea

The recommender system works by finding patterns in how participants rate items.  
- If two participants rated many of the same items as "highly relevant," and one of them rated another item highly, the system will predict that the other participant would likely also rate that item as highly relevant.  
- Using Funk SVD, we can estimate missing values in a large participant × item rating matrix.

---

## Getting Started
`library("recommenderlab")`
`library("Matrix")`
