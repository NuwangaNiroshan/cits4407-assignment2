# CITS4407 Assignment 2: Trending Videos Data Cleaning and Analysis

## Overview

This project contains two Bash scripts for CITS4407 Assignment 2.

The assignment follows a simple data-science workflow:

1. Clean an unclean CSV file
2. Analyse the cleaned CSV file

The scripts use Unix tools covered in the unit, mainly Bash and awk.

## Files

- `clean`  
  Checks and cleans `trending_videos_unclean.csv`

- `analyse`  
  Analyses `trending_videos_clean.csv`

- `trending_videos_unclean.csv`  
  Input file used for Question 1 testing

- `trending_videos_clean.csv`  
  Cleaned reference file used for Question 2 testing

- `.gitignore`  
  Ignores temporary testing files and final submission files

- `prompts.pdf`  
  Contains the AI prompt log for this assignment

## How to run

Give execute permission first:

```bash
chmod +x clean analyse

## Expected analysis output

```text
Most frequent video, ID: id4667
Mean number of views: 2355595.97
Max dislikes video, ID: id2798
Highest engagement rate video, ID: id2282, dated: 2018-01-04
Least sentiment rate video, ID: id2219, dated: 2017-12-13
```

## Cleaning rules

The `clean` script:

- checks that an input CSV file is provided
- checks that the input file exists
- checks that the input file has a `.csv` extension
- checks that the input file is not empty
- checks that the CSV header has 7 columns
- removes the `ratings_disabled` column
- removes rows with the wrong number of columns
- removes duplicate rows
- removes rows with a missing `video_id`
- removes rows with zero likes or dislikes
- removes the time part from `publish_date`

## Analysis results

The `analyse` script prints:

- the video ID with the most occurrences
- the mean number of views to two decimal places
- the video ID with the maximum number of dislikes
- the video ID and publish date with the highest engagement rate
- the video ID and publish date with the least sentiment rate

## Final submission note

The final LMS submission zip should contain only:

- `clean`
- `analyse`
- `prompts.pdf`
- `git_backup`

The CSV files, README file, `.gitignore`, and final zip file should not be included in the LMS submission package.