# Plagiarism-Detection-using-LSH

## Problem Statement

Plagiarism is a widespread issue in today's age of information. The extent of it can also vary from minor modification to outright copying. The task of finding similiar documents has some pitfalls.

* Brute-force comparison requires $O(n^2)$ comparisons which is not feasible if $n$ is large
* We need to account for word ordering since small pieces of a document can appear out of order in another document
* If the documents are large, they will not fit in main memory

## Solution

* Represent documents as sets of $n$-grams to account for word-ordering
* Use Min Hashing to convert sets into short signatures which fit in main memory
* Use Locality Sensitive Hashing to generate a small set of candidate pairs for comparison

**Algotrithms Used**:  Min Hashing, Locality Sensitive Hashing (LSH)

**Dataset**: https://data.mendeley.com/datasets/gz3hztwm5p/1

## Project Work Flow

1. Data pre-processing
2. File parsing and data extraction
3. **Converting text into sets using n-grams**
4. **Min-hashing the document sets to smaller signatures**
5. **LSH to find similar documents (images)**
6. Analyzing performance
