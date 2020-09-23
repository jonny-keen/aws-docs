# AWS Step Functions

## intro

- can build a workflow for a series of event-driven steps
- allows combining of lambdas with other AWS services

## features

### parallel workflows

- executes multiple branches of workflows with the same input
- same input, different steps

### map workflows

- executes the same steps of a workflow for multiple entries in an input array
- same steps, different input

## terminology

- 'State Machine' = workflow
- 'Task' = a 'State' within a workflow which represents a single unit of work that another AWS service carries out
- 'State' = an individual step in a workflow

## pricing

- 4,000 free workflow step executions per month
- $0.025 per 1,000 state transitions thereafter
