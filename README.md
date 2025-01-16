# Election Results Analysis Project

This Python project provides a comprehensive toolkit for analyzing election results across multiple constituencies. It includes functionality for vote tabulation, winner determination, and identification of close contests.

## Features

- Calculate total votes per political party
- Identify winning parties in each constituency
- Determine the overall election winner
- Calculate vote share percentages for each candidate
- Identify close contests based on customizable margin thresholds

## Requirements

- Python 3.x
- pandas

## Installation

1. Clone this repository:
bash
git clone <repository-url>
cd election-analysis


2. Install the required dependencies:
bash
pip install pandas


## Usage

The main functionality is provided through several key functions in the project:

### Calculate Total Votes Per Party
python
calculate_total_votes_per_party()

Returns a Series containing the total votes received by each party across all constituencies.

### Find Constituency Winners
python
find_constituency_winners()

Returns a Series showing which party won in each constituency.

### Determine Overall Winner
python
determine_overall_winner()

Returns the name of the party that received the highest total votes across all constituencies.

### Calculate Vote Share
python
calculate_vote_share()

Returns a DataFrame with vote share percentages added for each candidate.

### Identify Close Contests
python
identify_close_contests(margin_threshold=12)

Returns a DataFrame containing information about constituencies where the margin of victory was below the specified threshold (default 12%).

## Data Format

The system expects election data in the following format:

python
data = {
    'Constituency': ['District1', 'District2', ...],
    'Party': ['Party A', 'Party B', ...],
    'Candidate': ['John Smith', 'Jane Doe', ...],
    'Votes': [1500, 1200, ...]
}


## Example Output


Total votes per party:
Party A    5200
Party B    5000
Party C    4000

Constituency winners:
District1    Party A
District2    Party B
District3    Party A

Vote shares:
Constituency    Party    Candidate  Votes  Vote_Share
District1      Party A  John Smith   1500   42.857143
District1      Party B   Jane Doe    1200   34.285714
...

Close contests (margin < 12%):
Constituency    Margin   Winner  Runner_up
District1     8.571429  Party A   Party B
District2     3.333333  Party B   Party A
District3     2.127660  Party A   Party B
