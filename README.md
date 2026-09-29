# Exploring NYC Public School Test Result Scores

## Overview

This project analyzes SAT performance across New York City public high schools. The SAT is a standardized test with three sections — reading, math, and writing — each worth up to 800 points. The analysis answers three key questions that are useful for policymakers, educators, researchers, and parents.

## Dataset

The dataset `schools.csv` contains information about NYC public schools, including:

| Column | Description |
|---|---|
| `school_name` | Name of the school |
| `borough` | NYC borough (Manhattan, Brooklyn, Queens, Bronx, Staten Island) |
| `building_code` | Building code |
| `average_math` | Average math SAT score |
| `average_reading` | Average reading SAT score |
| `average_writing` | Average writing SAT score |
| `percent_tested` | Percentage of students tested |

## Objectives

1. Identify schools with excellent math results (average math score ≥ 640, which is 80% of 800).
2. Find the top 10 performing schools based on combined SAT scores (math + reading + writing).
3. Determine which borough has the largest standard deviation in combined SAT scores.

## Approach

- Loaded the dataset with pandas.
- Filtered schools with `average_math >= 640` for the best math results.
- Created a new column `total_SAT` by summing the three section scores.
- Sorted and selected the top 10 schools by `total_SAT`.
- Grouped by borough to compute the number of schools, average SAT, and standard deviation of SAT.
- Identified the borough with the largest standard deviation and rounded numeric values to two decimal places.

## Results

### Best Math Schools (average_math ≥ 640)

The top schools include:
- Stuyvesant High School (754)
- Bronx High School of Science (714)
- Staten Island Technical High School (711)
- Queens High School for the Sciences at York College (701)
- High School for Mathematics, Science, and Engineering at City College (683)
- Brooklyn Technical High School (682)
- Townsend Harris High School (680)
- High School of American Studies at Lehman College (669)
- New Explorations into Science, Technology and Math High School (657)
- Eleanor Roosevelt High School (641)

### Top 10 Schools by Total SAT

| School | Total SAT |
|---|---|
| Stuyvesant High School | 2144 |
| Bronx High School of Science | 2041 |
| Staten Island Technical High School | 2041 |
| High School of American Studies at Lehman College | 2013 |
| Townsend Harris High School | 1981 |
| Queens High School for the Sciences at York College | 1947 |
| Bard High School Early College | 1914 |
| Brooklyn Technical High School | 1896 |
| Eleanor Roosevelt High School | 1889 |
| High School for Mathematics, Science, and Engineering at City College | 1889 |

### Borough with Largest Standard Deviation

| Borough | num_schools | average_SAT | std_SAT |
|---|---|---|---|
| Manhattan | 89 | 1340.13 | 230.29 |
