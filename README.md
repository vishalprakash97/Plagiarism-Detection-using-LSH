# Plagiarism-Detection-using-LSH

## Introduction

Plagiarism is a widespread issue in today's age of information. It refers to the unauthorized usage of another author's work and representing it as one's own effort without providing due credit. The extent of plagiarism can also vary from minor modification of another work to outright copying. The scientfic community has put in significant effort to design and produce efficient solutions to quickly identify cases of plagiarism at scale since brute-force comparison is not feasible.

For $n$ documents, to compare the similarity between each pair, we will need to make  $O(n^2)$ comparisons which is not advisable if $n$ is large. Additionally, to represent a document, we tend to convert documents into single dimension arrays which tell us whether a single word/character or a sequence of words/characters are present in a document along with their frequencies. It is these arrays which we compare when matching pairs of documents. However these arrays tend to be sparse which leads to large memory consumption. Hence efforts have been made to reduce the memory requirements of these naive methods.

Min-Hashing and Locality Sensitive Hashing (LSH) are two algorithms that can be used to reduce the time and space consumed to efficiently and quickly identify documents which show high levels of similarity.

In this project, we attempt to make use of these two algorithm to develop a plagiarism detector. Given a list of of original documents, the solution will learn the text corpus representing these documents. We then provide a list of documents which may or may not be duplicates of these original "source" documents. The "suspicious" documents are then compared with the source files and tagged as plagiarism if the level of similarity exceeds a threshold.

## Dataset

The dataset we are using has been obtained from https://data.mendeley.com/datasets/gz3hztwm5p/1 which was put together to help the research community develop techniques to detect plagiarism in documents containing images and their associated text. The intuition here is that if an image in a document has been plagiarised, the text pertaining to the image should also be similar. This text includes the caption below the image and text in the main paragraphs that refer to the image. The dataset also includes text which explains the structure of the image but this has not been used as a part of the project. There are 122 source text files, one each for every source image, and 146 suspicious text files, one each for every suspicious image which may or may not be a plagiarism of one of the source images. We also have an annotation .xml file for each suspicious file which tells us whether the suspicious image is truely a plagiarism or not.

## Process Flow of Project
The steps we followed to implement the project are as follows:

1. Data pre-processing such as reading in files and associated annotations
2. File parsing and data extraction
3. Converting text into sets using n-grams
4. Min-hashing the document sets to smaller signatures
5. LSH to find similar documents (images)
6. Understanding performance
