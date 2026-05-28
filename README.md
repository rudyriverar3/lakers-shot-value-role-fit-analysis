# lakers-shot-value-role-fit-analysis

NBA shot value analysis of Austin Reaves’ 2025-26 season, evaluating expected shot quality, scoring efficiency, and role fit within the Lakers’ roster context.

Project Overview
This project analyzes Austin Reaves’ 2025-26 shot profile using NBA shot chart data. The goal is to evaluate where Reaves creates offensive value, how his actual scoring compares to expected shot quality, and how his skill set may fit within different Lakers roster constructions.

The analysis focuses on shot type, shot zone, points per shot, expected shot value, and role fit as a complementary starter, secondary creator, or sixth-man option.

Main Questions
What does Austin Reaves’ 2025-26 shot profile look like?
Where does he create the most value as a scorer?
How does his actual shot value compare to expected shot value?
Which zones are high-value or low-value?
Does his shot profile support a role as a complementary starter, secondary creator, or sixth man?
Tools Used
Python
pandas
numpy
matplotlib
seaborn
scikit-learn
nba_api
Jupyter Notebook
Methodology
This project uses shot-level NBA data to evaluate Austin Reaves’ offensive shot profile.

Main steps:

Pulled Austin Reaves’ 2025-26 shot chart data.
Cleaned and standardized shot-level data.
Created key features including made/missed flag, shot value, actual points, shot zone, and time remaining.
Summarized shot value by shot type and court zone.
Visualized shot volume, efficiency, and shot location.
Built a logistic regression model to estimate expected make probability.
Converted expected make probability into expected points.
Compared actual points to expected points by shot type and zone.
Interpreted the results through a Lakers roster-fit lens.
Expected points were calculated as:

expected points = expected make probability × shot value

Points above expected were calculated as:

points above expected = actual points - expected points

Key Findings
Reaves added value above expectation on three-point attempts.
His three-point attempts produced 1.079 actual points per shot compared with 1.050 expected points per shot.
His two-point attempts were efficient overall, but almost exactly in line with expected shot quality.
His strongest value areas were the left corner three, left-side above-the-break three, and restricted area.
His lower-performing areas were right-side above-the-break threes and non-restricted paint attempts.
His shot profile suggests scalable offensive value because his best areas are rim attempts and three-point shooting.
Role Fit Interpretation
Austin Reaves’ shot profile suggests he can provide value in multiple roster contexts.

As a complementary starter, his three-point shooting and ability to attack closeouts allow him to fit next to high-usage stars.

As a secondary creator, his rim pressure and restricted-area scoring give him value when attacking defensive rotations.

As a sixth man, his ability to generate value from both the rim and three-point line suggests he could help stabilize second-unit offense while still fitting into closing lineups depending on matchup and roster construction.

The main usage recommendation is to emphasize rim pressure, left-side three-point opportunities, and advantage-based attacks while monitoring right-side above-the-break threes and non-restricted paint attempts.

Limitations
This version uses an expected shot value model trained only on Austin Reaves’ 2025-26 shot attempts. Because of that, the expected values reflect patterns within his own shot profile rather than a league-wide NBA baseline.

A stronger future version would train the expected shot model on all 2025-26 NBA shots and then apply that model to Reaves. That would allow his shot-making and shot quality to be compared against league-average expectations for similar shots.

Some shot zones also had small sample sizes, especially corner threes and midrange areas. These results should be interpreted carefully.

The role-fit scenarios are not trade predictions. They are basketball context scenarios used to evaluate how Reaves’ shot profile may scale next to different types of high-usage players.

Future Improvements
Add interactive 3D shot charts using Plotly
Build a 3D points-above-expected court surface
Expand the analysis to other Lakers players
Train a league-wide expected shot value model
Build a Streamlit dashboard with player and shot-zone filters
Compare Reaves’ role fit next to different roster archetypes
Repository Contents
Austin_Reaves_2025_26_Shot_Value_and_Role_Fit.ipynb: main analysis notebook
README.md: project overview and findings
Author
Created by Rudy Rivera
