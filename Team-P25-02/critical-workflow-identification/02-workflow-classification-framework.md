<a id="section-2"></a>

# 2. Workflow Classification Framework

<a id="section-3"></a>

## 2.1 Critical Workflow Definition

A workflow is critical to PEERS if its failure prevents a primary professor or student task, compromises the integrity or confidentiality of essential data or access controls, or blocks another required workflow. Every critical workflow must have observable outcomes that support verification of functional preservation through regression or end-to-end testing.

A workflow qualifies as critical when any one of the following conditions applies:

Primary-task impact: failure prevents a professor or student from completing an essential PEERS task.

Data or access impact: failure can cause loss or corruption of essential data, incorrect results, unauthorized access, or disclosure of confidential evaluation information.

Dependency impact: failure blocks another required workflow from completing correctly.

<a id="section-4"></a>

## 2.2 Supporting Workflow Definition

A supporting workflow enables, prepares, or completes part of a critical workflow but is not necessarily a primary user goal by itself. Supporting does not mean optional: if a supporting workflow is required for a critical workflow to function correctly, its behavior must still be preserved within that dependency chain.

<a id="section-5"></a>

## 2.3 Classification Status

The classifications in this document are proposed for sponsor review. They are based on the approved PEERS functional baseline, project specification, the Technical Assessment, and the Application Architecture Review. If sponsor confirmation changes the supported functional baseline, the workflow classifications should be updated accordingly.

<br>
