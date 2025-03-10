# Nielsenik-Work

📊 Foxintelligence Technical Test – Digital & New Verticals

🖋️ Introduction

This repository contains my solution for the Nielsenik Technical Test

The project is divided into two main tasks:

- Enriching the dataset by adding app titles and editor names.

- Analyzing the impact of Covid confinement on in-app purchases.

# Dataset Enrichment Approach

To answer the first question, we need to join the two excel tables. The problem is that there is no common factor between the two tables except for the images behind each URL. 
In order to correctly match the logo between the two tables, we need to use a python code that will assign an hash record, to generate unique identifiers for each image and then compare the hash record with each images from the external table. 

I implemented a first Jupyter notebook (Final.ipynb) that processes the dataset as follows:

Image Hashing: Each image URL was hashed using a perceptual hashing algorithm to generate unique identifiers.

Matching Process: The hashes were compared against those from the external data source to find the closest matches.

Table Join: Once the app title and editor names were retrieved, a simple XLOOKUP function was applied using the URLs to join the enriched data with the main table.

This approach ensures a reliable and automated way to map the correct app information despite inconsistencies in image URLs.
