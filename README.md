Lab Assignment 4: Airline Crew Scheduling - NP-Hard Problem Solving

Course: Design and Analysis of Algorithms Lab (ENCA351)

Program: BCA (AI&DS)

Semester: V (2025-26)

Faculty: Dr. Aarti

📌 Project Overview

This project implements a solution for the Airline Crew Scheduling problem, a classic example of an NP-Hard resource allocation problem. The goal is to assign a set of flights to available crew members while adhering to strict operational constraints.

Because finding an optimal schedule is computationally expensive for large datasets, this project demonstrates a Backtracking (Constraint Satisfaction) approach to find valid assignments and analyzes the computational limits of this method.

🚀 Problem Statement

We are given a set of flights and a set of crew members. We must assign flights such that:

No Overlaps: A crew member cannot fly two overlapping flights at the same time.

Rest Period: A minimum rest time (e.g., 1 hour) is required between the end of one flight and the start of the next for the same crew member.

Input Data Format

Flights: (Flight ID, Start Time, End Time)

Crew: ['C1', 'C2', 'C3']

🛠️ Solution Approach

The project uses a Recursive Backtracking algorithm:

Sort Flights: Flights are sorted by start time to streamline the assignment process.

Constraint Checking: Before assigning a flight, the algorithm checks:

Does the flight overlap with the crew's current schedule?

Is there enough rest time after their last flight?

Recursion: The algorithm attempts to assign the current flight to a crew member and recursively moves to the next flight.

Backtracking: If a flight cannot be assigned to any crew member, the algorithm "backtracks" (undoes the previous assignment) and tries a different path.

📊 Complexity Analysis

This problem is NP-Hard. The backtracking approach explores the state space of possible assignments.

Time Complexity: $O(k \times 2^n)$

Where $n$ is the number of flights and $k$ is the number of crew members.

As shown in the project profiling, execution time grows exponentially as $n$ increases.

Space Complexity: $O(n)$ (recursion stack depth).

⚙️ Setup and Installation

Prerequisites

Python 3.x

Jupyter Notebook or VS Code

Installation Steps

Clone the repository:
(Replace YOUR_USERNAME with your actual GitHub username)

git clone [https://github.com/YOUR_USERNAME/airline-crew-scheduling.git](https://github.com/YOUR_USERNAME/airline-crew-scheduling.git)
cd airline-crew-scheduling


Install dependencies:

pip install -r requirements.txt


(Note: This project requires matplotlib for visualization and memory_profiler for analysis)

Run the Notebook:
Open crew_scheduling_notebook.ipynb in Jupyter or VS Code and run all cells.

📈 Visualization & Profiling

The project includes visualization tools to analyze the schedule and the algorithm's performance.

1. Gantt Chart

Visualizes the final schedule, showing which crew member is flying at what times.

2. Performance Analysis

A graph plotting Execution Time vs. Number of Flights, demonstrating the exponential growth of the backtracking algorithm.

📚 References

Introduction to Algorithms - Cormen et al. (CLRS) for Backtracking and NP-Completeness concepts.

Lab Assignment 4 Problem Statement - School of Engineering & Technology, K.R. Mangalam University.

Python Documentation - matplotlib and itertools.

Submitted by Rohit_Kumar(2301201067) for ENCA351.