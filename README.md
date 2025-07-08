# Project Leader Assignment Optimization

This project is based on a case study involving optimal assignment of scientists to research projects in order to maximize total preference scores. The problem is formulated as a binary integer programming model and solved using **Gurobi** in Python.

## Case Overview

A pharmaceutical firm must assign scientists to lead five research projects. Each scientist has a preference score for each project, and some constraints apply based on experience, personal limitations, and strategic decisions.

The goal is to **maximize the total preference points** across all project assignments while satisfying the specific constraints outlined in each scenario.

## Scenarios Modeled

All scenarios are solved in one Jupyter notebook:

### (a) Baseline Assignment
- Assign each of the 5 projects to 5 doctors
- Each project must be assigned to exactly one doctor

### (b) Staff Reduction
- Only 4 scientists available; one scientist must lead 2 projects

### (c) Two-Project Allowance
- Dr. Zuner or Dr. Mickey can lead 2 projects, others only 1

### (d) Updated Bids
- Dr. Zuner updates her preference scores

### (e) Addition of Dr. Rollins
- Dr. Rollins joins the team; all 5 projects to be assigned to 5 scientists

### (f) Constraints on Eligibility
- Some scientists cannot lead certain projects based on background
- New bid values considered for constrained doctors

### (g) Complex Projects (Hope and Release)
- These two projects must each be assigned to **two scientists**
- Two new doctors (Dr. Arriaga and Dr. Santos) are hired
- Religious constraints prevent Arriaga and Santos from leading Project Choice

## Approach

- **Binary decision variables**: 1 if a doctor is assigned to a project, 0 otherwise
- **Objective function**: Maximize total preference score
- **Constraints** vary per scenario and are implemented using `model.addConstr()`

## Tools Used

- Python
- Gurobi Optimizer
- Jupyter Notebook

## Files

- `PROJECT ASSIGNMENT.ipynb`: Full implementation of all scenarios
- `README.md`: Project summary

## Output

The notebook prints:
- Assignment of each project to the most suitable doctor(s)
- The maximized preference score for each scenario
