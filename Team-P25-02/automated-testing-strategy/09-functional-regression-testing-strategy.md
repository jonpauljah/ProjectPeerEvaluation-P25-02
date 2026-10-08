<a id="section-9"></a>

# Functional Regression Testing Strategy

| Area | Requirement |
| --- | --- |
| Workflow coverage | Create one or more automated checks for every sponsor-approved priority workflow. |
| Expected behavior | Do not silently treat known broken behavior as expected behavior; document it as a defect and confirm the desired behavior. |
| Defect regression coverage | When a material defect is fixed, add or update a regression test that would fail if the defect returns. |
| Before-merge validation | Run the highest-value regression checks before merge. |
| Extended validation | If some scenarios are too slow for every pull request, assign them to a documented extended CI or release-validation stage. |
| Traceability | Link regression tests back to requirements and defects through the RTM. |
