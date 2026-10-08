<a id="section-7"></a>

# Unit Testing Strategy

| Area | Requirement |
| --- | --- |
| Test selection | Prioritize pure or isolated logic that has clear inputs and expected outputs. |
| Authentication and authorization | Cover authentication and authorization decisions. |
| Evaluation links and tokens | Cover evaluation-link/token creation and validation. |
| CSV processing | Cover CSV parsing and validation rules. |
| Rubrics and scoring | Cover rubric and scoring/aggregation logic. |
| Business rules | Cover eligibility and other reusable business rules discovered in the codebase. |
| Test cases | Use positive, negative, boundary, and invalid-input cases. |
| Execution speed | Keep unit tests fast enough to run on every required CI execution. |
