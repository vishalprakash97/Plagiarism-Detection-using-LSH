# Plagiarism-Detection-using-LSH

## Introduction

Plagiarism is a widespread issue in today's age of information. The extent of it can also vary from minor modification to outright copying. The scientfic community has put in significant effort to design and produce efficient solutions to quickly identify cases of plagiarism at scale since brute-force comparison is not feasible.

For $n$ documents, to compare the similarity between each pair, we will need to make  $O(n^2)$ comparisons which is not advisable if $n$ is large. Additionally, documents are represented as vectors which are sparse leading to large memory consumption. Hence efforts have been made to reduce the memory requirements of these naive methods.

**Algotrithms Used**:  Min Hashing, Locality Sensitive Hashing (LSH)

**Dataset**: https://data.mendeley.com/datasets/gz3hztwm5p/1

## Process Flow of Project

1. Data pre-processing
2. File parsing and data extraction
3. **Converting text into sets using n-grams**
4. **Min-hashing the document sets to smaller signatures**
5. **LSH to find similar documents (images)**
6. Analyzing performance
