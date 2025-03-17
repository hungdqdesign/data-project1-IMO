# IMO Data Analysis Project Proposal

## Authors: Ngo Sy Trung & Doan Quang Hung

### 1. Dataset Description

We are analyzing a dataset from the International Mathematical Olympiad (IMO), sourced from official IMO records spanning decades of competition history. The dataset comprises three CSV files:

* **country_results_df.csv**: 3,780 rows × 18 columns, containing country-level performance metrics (e.g., team scores, medal counts).
* **individual_results_df.csv**: 21,707 rows × 13 columns, detailing individual contestant results (e.g., scores per problem, rankings, awards).
* **timeline_df.csv**: 65 rows × 10 columns, providing historical IMO data (e.g., host countries, years).

This comprehensive dataset offers a rich foundation for exploring mathematical competition trends over time.

### 2. Reason for Selection

We selected this dataset because it:

* Integrates individual, team, and historical perspectives, enabling multi-dimensional analysis.
* Combines numerical data (e.g., scores, rankings) with categorical data (e.g., countries, awards), supporting diverse analytical approaches.
* Facilitates cross-file data merging for deeper insights.
* Offers a unique lens into global mathematics education and competitive performance.

### 3. Research Questions

#### Q1: How do individual rankings influence team performance?

* **Objective**: Determine whether team success hinges on standout individual performers or consistent group performance.
* **Motivation**: Understanding this dynamic could inform team selection strategies.

#### Q2: Does hosting the IMO affect the performance of domestic contestants?

* **Objective**: Investigate the presence and persistence of a "home advantage" effect.
* **Motivation**: This could reveal environmental influences on competitive outcomes.

### 4. Analysis Plan

#### For Q1: Individual Rankings and Team Performance

* **Data Preparation**:
   * Merge individual_results_df.csv (variables: individual_rank, total, p1-p7, award) with country_results_df.csv (variables: awards_gold, awards_silver, awards_bronze, team_size_all).
   * Compute team score distributions and individual contribution metrics.

* **Analysis**:
   * Calculate correlations between individual rankings and team medal counts.
   * Assess the impact of top scorers versus median performers on team success using regression or contribution analysis.

* **Visualization**:
   * Scatter plots: Top performer scores vs. team medals.
   * Box plots: Team score distributions by medal type.

#### For Q2: Hosting Impact on Domestic Performance

* **Data Preparation**:
   * Merge timeline_df.csv (variables: host country, year) with country_results_df.csv (variables: awards, p1-p7).
   * Create time-relative variables (e.g., years before/during/after hosting).

* **Analysis**:
   * Compare host country performance metrics (e.g., average scores, medal counts) across hosting and non-hosting years using statistical tests (e.g., t-tests).
   * Explore regional patterns or persistence of effects over time.

* **Visualization**:
   * Time series plots: Performance trends before, during, and after hosting.
   * Bar charts: Comparative performance of host vs. non-host countries.

### 5. External Data Integration

To enrich our analysis, we plan to incorporate:

* **GDP per capita**: To contextualize economic influences on performance.
* **Educational investment data**: To explore links between education funding and IMO success.
* **Geographic classifications**: To examine regional performance trends.

These external datasets will be merged with our IMO data using country and year as keys, enhancing our understanding of broader socio-economic factors.