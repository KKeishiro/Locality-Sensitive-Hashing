# Locality-Sensitive-Hashing
Approximate nearest neighbour with Locality Sensitive Hashing

## Description
The goal of this project is detecting near-duplicate html pages. 
Suppose we want to write our own search engine. For reliability reasons, many web pages store duplicates or near duplicate versions of the same information.
Our task is to develop an efficient method to to detect whether a pages are near-duplicates of each other so that our search engine does not present the user redundant search results.

## Dataset
We will use Jaccard similarity based on the page features as the similarity metric. Two given text files:

1. **handout_shingles.txt**: Each line contains the features for one page file and is formatted as follows: PAGE_XXXXXXXXX followed by a list of space delimited integers in range [0, 8192]. You can consider them equivalent to shingles in the context of near-duplicate document retrieval.
2. **handout_duplicates.txt**: Each line contains a pair of near duplicates (pages that are at least 85% similar according to the Jaccard similarity). Each line is a tab-delimited pair of integers where the first integer is always smaller. This file is used to measure the error of your output as described below.
